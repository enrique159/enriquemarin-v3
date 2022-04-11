<template>
  <header class="container">
    <div class="logo" @click="goHome">
      <img src="@/assets/memoji.png"/>
      <div class="logo-name ps-3">
        <h4>Enrique Marin</h4>
        <p>Personal website</p>
      </div>
    </div>

    <div class="nav-option">
      <RouterLink to="/portfolio">Portfolio</RouterLink>
      <RouterLink to="/aboutme">About me</RouterLink>
      <RouterLink to="/skills">Skills</RouterLink>
      <RouterLink to="/">Social media</RouterLink>
      <RouterLink class="lets-talk" to="/contact">Let's Talk <i class="ri-arrow-right-line ms-2"></i></RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<script>
export default {
  methods: {
    goHome() {
      this.$router.push('/')
    }
  },
}
</script>

<style lang="scss">
@import '@/styles/general.scss';

#app {
  height: fit-content;
  min-height: 100vh;
  background: rgba(37, 44, 67, 0.5);
  backdrop-filter: blur(150px);
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;

  .logo {
    height: 60px;
    display: flex;
    align-items: center;
    cursor: pointer;
    img {
      height: 100%;
    }
    .logo-name {
      h4 {
        font-size: 1.4rem;
        font-weight: 800;
        color: #fff;
        transition: 0.1s ease-in-out;
        margin: 0;
      }

      p {
        font-size: 1rem;
        font-weight: 300;
        color: #B7B7B7;
        transition: 0.1s ease-in-out;
        margin: 0;
      }
    }
    &:hover {
      .logo-name {
        h4 {
          padding-left: 12px;
        }
        p {
          padding-left: 6px;
        }
      }
    }
  }

  // Nav options
  .nav-option {
    display: flex;
    align-items: center;
    width: fit-content;
    column-gap: 3rem;
    a {
      text-decoration: none;
      transition: 0.2s ease-in-out;
      color: #B7B7B7;
      font-size: 1rem;
      font-weight: 500;
      &:hover {
        cursor: pointer;
        color: white;
      }
    }
    .lets-talk {
      background: #fff;
      border-radius: 5px;
      padding: 0.3rem 1rem;
      font-weight: 500;
      color: #000;
      display: flex;
      align-items: center;
      &:hover {
        cursor: pointer;
        background: #dfdfdf;
        color: #000;
      }
    }
  }
}
</style>
