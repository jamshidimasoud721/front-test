<template>
  <div class="contact">
    <div class="contact-header">
      <h2>Contact Us</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, autem.</p>
    </div>
    <div class="contact-content">
      <form action="">
        <div class="contact-info">
          <input type="text" placeholder="Name">
          <input type="email" placeholder="Email">
        </div>
        <textarea placeholder="Message"></textarea>
      </form>
      <button class="btn btn-dark btn-big">Send Message</button>
    </div>
  </div>

</template>

<script>
export default {

}
</script>

<style>
.contact {
  background-color: #3cadd4;
  color: #ffffff;
  padding: 100px 0;
}

.contact-header {
  text-align: center;
  margin-bottom: 80px;
}

.contact-header h2 {
  font-size: 40px;
  margin-bottom: 20px;
}

.contact-header p {
  font-size: 20px;
}

.contact-content {
  text-align: center;
}

.contact-info{
  display: flex;
  gap: 10px;
  justify-content: center;
}
input[type="text"],
input[type='email'] {
  background-color: #fff;
  color: #444;
  border: none;
  border-radius: 4px;
  padding: 15px 11px;
  width: 25%;
}

textarea {
  background-color: #fff;
  color: #444;
  border: none;
  border-radius: 4px;
  height: 200px;
  padding: 15px 25px;
  width: 50%;
  margin-top: 20px;
}

.contact-content button {
  margin-top: 20px;
}

::placeholder {
  color: #858585!important;
  font-size: 15px;
}

.btn {
  padding: 10px 20px;
  border-radius: 30px;
  border: 0;
  cursor: pointer;
  text-align: center;
  font-size: 16px;
  color: #ffffff;
}

.btn-dark {
  background-color: #383b43;
  color: #ffffff !important;
}

.btn-big {
  font-size: 20px !important;
  padding: 17px 35px;
}
</style>