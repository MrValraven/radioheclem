<template>
  <section :style="{ background: getImgURL('radio.jpg') }"></section>
  <div class="card">
    <h1>Radio Heclem</h1>
    <p>Disponível em breve</p>
    <div class="socials">
      <i class="fab fa-instagram">
        <a
          href="https://www.instagram.com/radioheclem/"
          target="_blank"
          rel="noopenner noreferrer"
        ></a>
      </i>
      <i class="fab fa-facebook-square">
        <a
          href="https://www.facebook.com/RadioHECLEM"
          target="_blank"
          rel="noopenner noreferrer"
        ></a>
      </i>
    </div>
  </div>
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
  filter: blur(5px);
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
}
</style>
