<template>
  <div id="app" class="wrapper">
    <nav class="nav_bar">
      <ul>
        <li><router-link to="/contacts">Contacts</router-link></li>
        <li><router-link to="/guides">Guides</router-link></li>
        <li><router-link to="/templates">Templates</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/news">News</router-link></li>
      </ul>
    </nav>
    <section class="start_section">
      <img src="/src/assets/img/main_pic.jpeg" alt="">
       <div class="first_section_container">
         <h1>{{ msg }}</h1>
       </div>
    </section>
    
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Vue.js App'
    }
  }
}
</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.wrapper {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  position: absolute;
  background-color: whitesmoke;
}


.nav_bar {
  position: fixed;
  width: 100%;
  height: 50px;
  background-color: rgba(144,219,255,0.4);
  top: 0;
  z-index: 10;
}

.nav_bar ul li{
  list-style-type: none;
  float: right;
}

.nav_bar a {
  display: inline;
  position: relative;
  right: 0;
  text-decoration: none;
  color: black;
  padding: 0 15px 0 15px;
  line-height: 3.02;
}

.nav_bar a:before{
  content: "";
  left: 5px;
  width: 0%;
  height: 1.5px;
  background-color: rgba(0,0,0, 0.3);
  position: absolute;
  transform: translateY(33px);
  transition: .3s;
}

.nav_bar a:hover:before{
  content: "";
  width: 90%;
  height: 1px;
  background-color: rgba(0,0,0, 0.3);
  position: absolute;
  transform: translateY(33px);
  transition: .3s;
}

.start_section {
  width: 100%;
  height: 40%;
  background-color: rgb(202, 227, 255);
  margin: 0;
  position: relative;
}

.start_section img{
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: 1; 
}

.first_section_container {
  background-color: rgba(144,219,255,0);
  height: 100%;
  width: 70%;
  margin: 0 auto;
}

.first_section_container h1 {
  text-align: center;
  line-height: 16;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-weight: normal;
  position: relative;
  z-index: 3;
  height: 100%;
}


</style>
