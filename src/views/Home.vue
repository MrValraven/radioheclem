<template>
  <section :style="{ background: getImgURL('radio.jpg') }">
    <div class="card">
      <h1>Rádio HECLEM</h1>
      <p>Disponível em breve</p>
      <div class="socials">
        <a
          href="https://www.instagram.com/radioheclem/"
          target="_blank"
          rel="noopenner noreferrer"
          ><i class="fab fa-instagram"></i>
        </a>

        <a
          href="https://www.facebook.com/RadioHECLEM"
          target="_blank"
          rel="noopenner noreferrer"
          ><i class="fab fa-facebook-square"></i
        ></a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Home",
  methods: {
    getImgURL(imageName) {
      return require("@/assets/" + imageName);
    },
  },
};
</script>

<style scoped lang="scss">
section {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: url("../assets/radio.jpg") no-repeat center center;
  background-size: cover;
}

.card {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 400px;
  height: 200px;
  padding: 20px;
  background: #1e1e1f;
  box-shadow: 0 8px 32px 0 #1e1e1f;
  backdrop-filter: blur(15.5px);
  -webkit-backdrop-filter: blur(15.5px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);

  h1 {
    font-size: 36px;
  }

  p {
    font-size: 20px;
    margin: 20px 0;
  }

  a {
    color: white;
    padding: 5px;
    margin: 10px 20px;

    i {
      font-size: 25px;
    }
  }
}

@media (max-width: 700px) {
  .card {
    width: 90vw;

    h1 {
      font-size: 30px;
    }
  }
}
</style>
