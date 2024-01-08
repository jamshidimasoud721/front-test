<template>
  <div class="about">
    <div class="container">
      <div class="about-header">
        <h2>About Us</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, autem.</p>
      </div>
      <div class="about-content">
        <div class="profile">
          <img src="../../src/assets/img/profile_placeholder.gif" alt="">
          <h4>Lorem ipsum</h4>
          <p>Lorem ipsum dolor</p>
        </div>
        <div class="profile">
          <img src="../../src/assets/img/profile_placeholder.gif" alt="">
          <h4>Lorem ipsum</h4>
          <p>Lorem ipsum dolor</p>
        </div>
        <div class="profile">
          <img src="../../src/assets/img/profile_placeholder.gif" alt="">
          <h4>Lorem ipsum</h4>
          <p>Lorem ipsum dolor</p>
        </div>
        <div class="profile">
          <img src="../../src/assets/img/profile_placeholder.gif" alt="">
          <h4>Lorem ipsum</h4>
          <p>Lorem ipsum dolor</p>
        </div>
      </div>
      <div class="about-footer">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam dolore illum, temporibus veritatis
          eligendi, aliquam, dolor enim itaque veniam aut eaque sequi qui quia vitae pariatur repudiandae ab dignissimos
          ex!</p>
      </div>
    </div>
  </div>
</template>

<style>
.about {
  text-align: center;
  padding: 100px 0;
}

.about-header h2 {
  font-size: 42px;
  color: #474747;
  margin-bottom: 12px;
}

.about-header p {
  font-size: 22px;
  color: #858585;
}

.about-content {
  border-bottom: 1px solid rgba(144, 144, 144, 0.25);
  border-top: 1px solid rgba(144, 144, 144, 0.25);
  margin: 60px auto;
  width: 90%;
  padding-top: 60px;
}

.about-content > * {
  float: left;
}

.about-content:after,
.about-content:before {
  content: '';
  display: block;
  clear: both;
}

.profile {
  width: 25%;
  margin-bottom: 60px;
}

.profile img {
  float: left;
  border-radius: 50%;
  /* margin-left: 15%; */
}

.profile h4 {
  margin-top: 20px;
}

.profile p {
  line-height: 25px;
}

.about-footer p {
  line-height: 25px;
  font-size: 15px;
  margin-bottom: 40px;
}

.about-footer {
  width: 65%;
  margin: 0 auto;
}
</style>