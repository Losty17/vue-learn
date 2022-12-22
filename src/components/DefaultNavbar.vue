<template>
  <div class="navbar">
    <div class="logo">
      <img src="../assets/logo.png">
      <span>kappke<br><span>.tech</span></span>
    </div>
    <div class="user">
      <img src="../assets/user.png">
    </div>
  </div>
</template>

<script>
export default {
  name: 'DefaultNavbar',
  props: {}
}
</script>

<style scoped>
.navbar {
  height: 72px;
  background: #000;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 32px;
}

.logo {
  height: 100%;
  display: flex;
  align-items: center;
}

.logo > img {
  height: 32px;
  pointer-events: none;
  user-select: none;
}

.logo > span {
  color: #fff;
  font-size: 24px;
  margin: 16px;
  font-family: monospace;
  user-select: none;
  text-align: right;
  line-height: .5;
}

.logo > span > span {
  font-size: 12px;
}

.user {
  height: 100%;
  display: flex;
  align-items: center;
}

.user > img {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  border: 2px solid white;
}
</style>