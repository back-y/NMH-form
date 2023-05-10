<template>
  <div class="div h-100" id="app">
    <div class="div container-fluid h-100">
      <div class="row h-100">
       
        <div class="div col-md-12 bg-img  h-100 d-flex justify-content-center align-items-center">
          <div class="div col-md-8 rounded px-5 py-4 shadow bg-white  text-left">
            <div class="div m-l-bg col-md-12 col-sm-12 col-lg-12 col-xs-12 ">
                <img src="./assets/m-logo.png" class="m-logo" alt="">
              </div>
            <SignupForm />

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import SignupForm from './components/SignupForm.vue'

 export default {
  name: 'App',
  components: {
    SignupForm
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.vue-bg{
  background: #bce5d0;
}
.bg-img{
  background:linear-gradient(rgba(194, 193, 193, 0.5),rgba(179, 179, 179, 0.5)) ,url(./assets/bg.jpg)center/cover no-repeat fixed;
}
.m-l-bg{
  background: #d4af37;
  height: 13rem !important;
}


@media (max-width: 1366px) {
  .m-logo {
  width: 15rem !important;
  margin-left: 28rem !important;
  }
}
@media (max-width: 992px) {
  .m-logo {
  width: 15rem !important;
  margin-left: 5rem !important;
  }
}


@media (max-width: 768px) {
  .m-logo {
  width: 15rem !important;
  margin-left: 2.5rem !important;
  }
}


@media (min-width: 1024px) {

.m-logo {
width: 15rem !important;
margin-left: 15rem !important;
/*
  margin-left: 18rem !important;
*/
}
}
</style>
