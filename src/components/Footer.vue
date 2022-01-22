<template>
  <footer>
    <p>Copyright &copy; 2022</p>
    <router-link to="/about">About</router-link>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
footer {
  margin-top: 30px;
  text-align: center;
  a {
    color: #333;
    text-decoration: none;
    margin-top: 20px;
    padding: 2%;
    color: #212121;
    font-size: 20px;
    transition: .25s all;
    &:hover{
      transform: translateX(2px);
      color: aqua;
    }
  }
}
</style>

