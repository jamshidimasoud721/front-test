<template>
  <div class="header">
    <div class="top-menu">
      <div class="logo">
        <div><h1>
          <a href="#">Good Things</a>
        </h1>
          <caption>Foundation</caption>
        </div>
        <img src="../../assets/img/fingerprint.svg" alt="fingerprint">
      </div>
      <div class="nav">
        <ul>
          <li>
            <router-link to="/">Home</router-link>
          </li>
          <li>
            <router-link to="/about">About</router-link>
          </li>
          <li>
            <router-link to="/contact">Contact</router-link>
          </li>
          <li>
            <button class="btn btn-primary ">Sign Up</button>
          </li>
        </ul>
      </div>
    </div>
  </div>

</template>

<script>
export default {}
</script>

<style scoped>

.logo {
  float: left;
  display: flex;
  flex-flow: row-reverse;
  align-items: center;
}

.logo img {
  width: 50px;
  height: 50px;
}

.nav {
  text-align: right;
}

.nav ul li {
  display: inline;
  padding: 0 15px;
}

.nav ul li a {
  color: #1f1c1c;
  transition: color .2s ease-in-out;
}

.nav ul li a:hover {
  color: #8d0606;
}

.top-menu {
  padding: 40px;
}

.header {
  background-color: #F5F5F5;
}

.btn {
  padding: 10px 20px;
  border-radius: 30px;
  border: 0;
  cursor: pointer;
  text-align: center;
  font-size: 16px;

}

.btn-primary {
  background-color: cadetblue;
  color: #ffffff;
}

h1 a{
  color: #1f1c1c;
}
</style>