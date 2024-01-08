<template>
  <div class="banner-content" v-bind:style="{backgroundImage:'url(' + imgUrl + ')'}">
    <h2>Get Online Week 2023</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
      magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
      consequat.</p>
  </div>
  <div class="services">
    <div class="container">
      <div class="services-header">
        <h2>What We Do ?</h2>
        <p>Lorem ipsum dolor sit amet, delectus consequatur, similique quia!</p>
      </div>
      <div class="services-content" >
        <div class="box" v-for="job in jobs" :key="job.id">
          <h4>{{ job.title[0].text }}</h4>
          <p>{{ job.summary[0].text }}</p>
          <router-link :to="{name:'details' , params:{id:job.id}}" class="btn btn-red">Read more</router-link>
        </div>
      </div>
    </div>
  </div>

</template>

<script>

export default {
  data() {
    return {
      jobs: [],
      imgUrl:''
    }
  },
  mounted() {
    fetch('https://reason-digital-test-front.prismic.io/api/v2/documents/search?ref=ZZx1CRAAACIAlxlZ&src=apibrowser#format=json')
        .then(res => res.json())
        .then(data => {
          this.imgUrl=data.results[0].data.banner.url;
          this.jobs = data.results[0].data.jobs
        })
        .catch(err => console.log(err.message))
  }

}
</script>

<style>

.banner-content {
  color: #ffffff;
  padding: 130px 20px;
  //background-image: url(../../src/assets/img/charity.jpg);
  background-position: center center;
  background-size: cover;
}

.banner-content h2 {
  font-size: 60px;
  line-height: 130px;
  background-color: cadetblue;
  width: 35%;
  margin-left: 10px;
  padding: 10px;
}

.banner-content p {
  color: cadetblue;
  font-size: 22px;
  margin-bottom: 50px;
  background-color: #F5F5F5;
  width: 30%;
  margin-left: 10px;
  margin-top: 5px;
  padding: 10px;
}

.btn-red {
  background-color: transparent;
  color: #8d0606 !important;
  border: 2px solid #1f1c1c !important;
}

.services {
  background-color: #065362;
  border-bottom: 1px solid rgba(144, 144, 144, 0.25);
  border-top: 1px solid rgba(144, 144, 144, 0.25);
  padding: 100px 20px;

}

.services-header {
  margin-bottom: 50px;
}

.services-header h2 {
  font-size: 42px;
  color: #F5F5F5;
  margin-bottom: 12px;
}

.services-header p {
  font-size: 22px;
  color: #F5F5F5;
}


.services-content {
  display: flex;
  gap: 25px;
}

.box {
  text-align: center;
  background-color: #fff;
  padding: 40px 30px;
  border-radius: 4px;
  width: calc(calc(100% / 3) - 82px);
  border: solid 1px rgba(144, 144, 144, 0.25);
  margin: 0 10px;
}


.box h4 {
  color: #858585;
  font-size: 20px;
  margin: 60px 0 30px 0;
}

.box p {
  line-height: 25px;
  margin-bottom: 20px;

}


@media only screen and (max-width: 835px) {
  .box {
    width: 100%;
    padding: 60px 0;
    margin: 10px 0;
  }
}

</style>