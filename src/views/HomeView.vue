<template>
  <div class="container">
    <div class="row py-5">
      <div class="col col-11 py-5">
        <p class="subtext-head animate__animated animate__fadeInDown">
          Hola! Welcome 👋
        </p>
        <div class="d-flex">
          <div class="contact-links">
            <a
              href="https://www.github.com/enrique159"
              target="_blank"
              class="animate__animated animate__fadeInDown"
              style="animation-delay: 0.1s"
            >
              <i class="ri-github-fill"></i>
            </a>
            <a
              href="https://www.linkedin.com/in/enriquemarin"
              target="_blank"
              class="animate__animated animate__fadeInDown"
              style="animation-delay: 0.2s"
            >
              <i class="ri-linkedin-line"></i>
            </a>
            <a
              href="https://dribbble.com/enriquemarin"
              target="_blank"
              class="animate__animated animate__fadeInDown"
              style="animation-delay: 0.3s"
            >
              <i class="ri-dribbble-fill"></i>
            </a>
          </div>
          <div class="main-text ps-5">
            <h2 class="animate__animated animate__fadeInDown">
              I'm Enrique Marin, a Frontend Web developer
            </h2>
            <p class="animate__animated animate__fadeInDown">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi
              lacinia posuere aenean quis sed. Ultrices nec quis tincidunt
              aliquam nulla sapien. Imperdiet sed mauris facilisis integer purus
              neque lacinia.
            </p>
          </div>
        </div>
      </div>
      <div class="col col-1 pt-5">
        <div class="features mb-4">
          <h4>+4</h4>
          <p>Years of Experience</p>
        </div>
        <div class="features mb-4">
          <h4>12</h4>
          <p>Production Projects up</p>
        </div>
        <div class="features mb-4">
          <h4>29</h4>
          <p>Public Repositories</p>
        </div>
      </div>
    </div>
    <div class="footer-image"></div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      message: "Welcome to Your Vue.js App",
    };
  },
};
</script>

<style lang="scss" scoped>
.contact-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 1rem;
  a {
    width: 48px;
    aspect-ratio: 1;
    background: rgba(102, 104, 121, 0.5);
    border: none;
    color: #fff;
    display: grid;
    place-items: center;
    cursor: pointer;
    border-radius: 50%;
    transition: 0.1s ease-in-out;
    margin-bottom: 0.7rem;
    font-size: 1.5rem;
    text-decoration: none;
    &:hover {
      background: rgba(102, 104, 121, 0.881);
    }
  }
}
.subtext-head {
  font-size: 1.5rem;
  font-weight: 500;
  color: #b7b7b7;
  transition: 0.1s ease-in-out;
  margin: 0;
}
.main-text {
  h2 {
    font-size: 5rem;
    font-weight: 700;
  }
  p {
    font-size: 1.2rem;
    font-weight: 400;
    color: #b7b7b7;
  }
}

.features {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  width: fit-content;
  text-align: right;
  h4 {
    font-size: 1.5rem;
    font-weight: 700;
    color: #ffffff;
    transition: 0.1s ease-in-out;
    margin: 0;
  }
  p {
    font-size: 1rem;
    font-weight: 300;
    line-height: 1rem;
    color: #b7b7b7;
    transition: 0.1s ease-in-out;
    margin: 0;
  }
}

.footer-image {
  position: fixed;
  bottom: 0;
  left: 0;
  background-image: url('@/assets/image-bg-min.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 120px;
  animation: openup 1s ease-in-out;
}

@keyframes openup {
  0% {
    height: 0px;
  }
  100% {
    height: 120px;
  }
}
</style>