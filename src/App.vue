<template>
  <div id="app" class="wrapper">
    <nav class="nav_bar">
      <i class="fa fa-btc"></i>
      <ul>
        <li><router-link to="/contacts">Contacts</router-link></li>
        <li><router-link to="/guides">Guides</router-link></li>
        <li><router-link to="/templates">Templates</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/news">News</router-link></li>
        <li><router-link to="/">Main</router-link></li>
      </ul>
    </nav>
    <section class="start_section">
      <img src="src/assets/img/main_pic.jpeg" alt="">
       <div class="first_section_container">
         <div class="fs_c">
           <div class="fs_c_middle">
             <div class="fs_c_in">
               <h1>{{ msg }}</h1>
             </div>
           </div>
         </div>
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
}


.nav_bar {
  position: fixed;
  width: 100%;
  height: 50px;
  background-color: rgba(144,219,255,0.9);
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
  top: 16px;
  right: 20px;
  text-decoration: none;
  color: black;
  padding: 0 15px 0 15px;
}

.nav_bar a:before{
  content: "";
  left: 5px;
  width: 0%;
  height: 1.5px;
  background-color: rgba(0,0,0, 0.3);
  position: absolute;
  transform: translateY(23px);
  transition: .3s;
}

.nav_bar a:hover:before{
  content: "";
  width: 90%;
  height: 1px;
  background-color: rgba(0,0,0, 0.3);
  position: absolute;
  transform: translateY(23px);
  transition: .3s;
}

.start_section {
  width: 100%;
  height: 50%;
  margin: 0;
  position: relative;
}

.start_section img {
  width: 100%;
  height: 100%;
  position: relative;
}

.start_section::before{
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: rgba(118, 157, 158, 0.5);
  top: 0;
  left: 0;
  z-index: 1;
}

.first_section_container {
  background-color: rgba(144,219,255,0);
  height: 100%;
  width: 70%;
  margin: 0 auto;
}

.first_section_container {
  z-index: 2;
  text-align: center;
  display: table;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  overflow: hidden;
}

.first_section_container .fs_c{
  display: table-row;
}

.first_section_container .fs_c .fs_c_middle{
  display: table-cell;
  vertical-align: middle;
}

.first_section_container .fs_c_in{
  display: inline-block;
}

.first_section_container .fs_c_in h1{
  font-weight: normal;
  z-index: 3;
  color: rgb(255, 255, 255);
}


.nav_bar .fa-btc {
  position: absolute;
  font-size: 1.5em;
  padding: 12px;
  transform: translateX(20vh);
  opacity: .8;
}



</style>
