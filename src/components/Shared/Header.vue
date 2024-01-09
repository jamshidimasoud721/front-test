<template>
  <div class="header">
    <div class="top-menu">
      <div class="logo">
        <div>
          <h1><a href="#">Good Things</a></h1>
          <caption>Foundation</caption>
        </div>
        <img src="../../assets/img/fingerprint.svg" alt="fingerprint">
      </div>
      <input type="checkbox" id="menu-toggle">
      <label for="menu-toggle" class="menu-icon">&#9776;</label>
      <div class="nav">
        <ul class="mobile-menu">
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
          <li><button class="btn btn-primary">Sign Up</button></li>
        </ul>
      </div>
    </div>
  </div>

</template>

<script>
export default {}
</script>
