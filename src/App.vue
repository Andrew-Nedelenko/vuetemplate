<template>
  <div id="app" class="wrapper">
    <nav class="nav_bar">
      <i class="fa fa-btc"></i>
      <i class="fa fa-bars"></i>
      <ul>
        <li><router-link to="/contacts">Contacts</router-link></li>
        <li><router-link to="/guides">Guides</router-link></li>
        <li><router-link to="/templates">Templates</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/news">News</router-link></li>
        <li><router-link to="/">Home</router-link></li>
      </ul>
    </nav>
    <nav class="hide_nav">
      <ul>
        <li><router-link to="/contacts">Contacts</router-link></li>
        <li><router-link to="/guides">Guides</router-link></li>
        <li><router-link to="/templates">Templates</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/news">News</router-link></li>
        <li><router-link to="/">Home</router-link></li>
      </ul>
    </nav>
    <section class="start_section">
      <img src="src/assets/img/main_pic.jpeg" alt="">
       <div class="first_section_container">
         <div class="fs_c">
           <div class="fs_c_middle">
             <div class="fs_c_in">
               <h1>{{ msg }}</h1>
               <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium cupiditate earum tempore. 
                 Eum blanditiis eos harum tenetur quaerat corporis, aliquam cumque eaque nemo et itaque. Quos accusamus blanditiis odit, 
                 dignissimos hic porro perspiciatis voluptas ut eveniet voluptate quia iste veniam nulla debitis, fugiat placeat praesentium 
                 ad modi recusandae. Ipsa, porro.</p>
                 <a href="#"><button>Buy Now</button></a>
                 <a href="#"><button>Free Trial</button></a>
             </div>
           </div>
         </div>
       </div>
    </section>
    <section class="main_section">
      <div class="first_section_container">
         <div class="fs_c">
           <div class="fs_c_middle">
             <div class="fs_c_in">
               <h2>Lorem ipsum dolor sit amet.</h2>
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
      msg: 'Lorem ipsum dolor sit amet.'
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
  transition: .3s;
  z-index: 1;
  overflow-y: scroll;
}


.wrapper::before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: rgba(0, 0, 0, 0.651);
  top: 0;
  left: 0;
  z-index: 10;
  margin: 0;
  display: none;
}
// .hide_wrap {
//   position: absolute;
//   height: 100%;
//   width: 100%;
//   top: 0;
//   left: 0;
//   background-color: rgba(0, 0, 0, 0.726);
//   z-index: 20;
// }

::-webkit-scrollbar {
    width: 10px;
    z-index: 1;
}
 
::-webkit-scrollbar-track {
    box-shadow: inset 0 0 6px rgba(0,0,0,0.5); 
    border-radius: 8px;
    z-index: 1;
}
 
::-webkit-scrollbar-thumb {
    border-radius: 8px;
    box-shadow: inset 0 0 6px rgba(0,0,0,0.5);
    background-color: rgba(105,204,199, 0.9); 
    z-index: 1;
}

.nav_bar {
  position: fixed;
  width: 100%;
  height: 50px;
  background-color: rgba(220, 255, 245, 0.9);
  top: 0;
  z-index: 10;
  box-shadow: 0.6px 0.6px 0.6px 0.6px rgb(87, 68, 68);
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

.fa-bars {
  position: absolute;
  top: 17px;
  right: 17px;
  display: none;
}

.start_section {
  width: 100%;
  height: 50%;
  margin: 0;
  position: relative;
  z-index: 4;
}

.start_section img {
  width: 100%;
  height: 100%;
  position: relative;
  display: none;
}

.start_section::before{
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: rgb(105, 204, 199);
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

.first_section_container .fs_c_in p{
  font-weight: normal;
  z-index: 3;
  padding: 10px 10% 20px 10%;
  color: rgb(255, 255, 255);
  font-size: 1.2em;
}

.first_section_container .fs_c_in button {
  width: 180px;
  height: 50px;
  border: 1px solid whitesmoke;
  background-color: rgba(245, 241, 24, 0);
  border-radius: 25px;
  margin: 0 5px 0 5px;
  text-transform: uppercase;
  transition: .3s;
  color: white;
}

:active, :hover, :focus {
    outline: 0;
    outline-offset: 0;
}

.first_section_container .fs_c_in button:hover{
  width: 180px;
  height: 50px;
  border: none;
  background-color: rgba(187, 255, 0, 0.952);
  border-radius: 25px;
  margin: 0 5px 0 5px;
  text-transform: uppercase;
  transition: .3s;
  cursor: pointer;
  color: rgba(0, 0, 0, 0.651);
}


.nav_bar .fa-btc {
  position: absolute;
  font-size: 1.5em;
  padding: 12px;
  transform: translateX(20vh);
  opacity: .8;
}

.main_section {
  width: 100%;
  height: 10%;
  position: absolute;
  overflow: hidden;
  margin: 0;
  display: none;
}

.hide_nav{
  top: 55px;
  right: -40%;
  position: fixed;
  width: 40%;
  height: 50vh;
  background-color:rgba(0, 0, 0, 0.788);
  z-index: 14;
  border-bottom-left-radius: 25px;
  border-top-left-radius: 25px;
  transition: .2s;
}

.hide_nav ul li{
  list-style-type: none;
  padding: 0.5rem;
  text-align: center;
  transform: translateY(37px);
}

.hide_nav a{
  text-decoration: none;
  color: rgb(255, 255, 255);
}

.hide_nav a:hover{
  text-decoration: none;
  color: rgb(255, 255, 255);
}



.hide_nav a:before{
  content: "";
  left: 5px;
  width: 0%;
  height: 1.5px;
  background-color: rgba(255, 255, 255, 0.3);
  position: absolute;
  transform: translateY(23px);
  transition: .3s;
}

.hide_nav a:hover:before{
  content: "";
  width: 90%;
  height: 1px;
  background-color: rgba(255, 255, 255, 0.3);
  position: absolute;
  transform: translateY(23px);
  transition: .3s;
}

@media (max-width: 700px) {
  .nav_bar {
  position: fixed;
  width: 100%;
  height: 50px;
  background-color: rgba(220, 255, 245, 0.9);
  top: 0;
  z-index: 10;
  box-shadow: 0.6px 0.6px 0.6px 0.6px rgb(87, 68, 68);
}

.nav_bar ul li{
  list-style-type: none;
  float: right;
}

.nav_bar a {
  display: none;
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

.fa-bars {
  position: absolute;
  top: 10px;
  right: 10px;
  display: block;
  transition: .3s;
  padding: 7px;
}
}

</style>
