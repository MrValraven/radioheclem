<template>
  <section>
    <div class="card" v-if="isLaunched">
      <img :src="getImgURL('logo-radio.png')" />
      <p>
        Estamos a afinar as vozes e a ligar os últimos cabos.<br />Prepara-te, a
        tua rádio está quase a chegar!
      </p>
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
  data() {
    return {
      isLaunched: true,
    };
  },
  methods: {
    getImgURL(imageName) {
      return require("@/assets/" + imageName);
    },
  },
};
</script>

<style scoped lang="scss">
$fontColor: #fc7532;

section {
  min-height: 100vh;
  max-width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #151415;
}

.card {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 80%;
  padding: 20px;

  img {
    width: 400px;
  }

  h1 {
    font-size: 36px;
  }

  p {
    font-size: 30px;
    font-weight: bold;
    color: $fontColor;
    text-transform: uppercase;
    margin: 20px 0 50px 0;
  }

  a {
    color: $fontColor;
    padding: 5px;
    margin: 10px 50px;

    i {
      font-size: 35px;
    }
  }
}

@media (max-width: 700px) {
  .card {
    width: 100%;

    img {
      width: 90%;
    }

    p {
      font-size: 24px;
    }
  }
}
@media (max-width: 300px) {
  .card {
    a {
      margin: 10px 20px;
    }
  }
}
</style>
