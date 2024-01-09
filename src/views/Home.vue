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
          <button class="btn btn-red">Read more</button>
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
    fetch('https://reason-digital-test-front.prismic.io/api/v2/documents/search?ref=ZZ2RtxEAACIAUwck&src=apibrowser#format=json')
        .then(res => res.json())
        .then(data => {
          this.imgUrl=data.results[0].data.banner.url;
          this.jobs = data.results[0].data.jobs
        })
        .catch(err => console.log(err.message))
  }

}
</script>

