<template>
  <div class="templates">
      <div class="catalog">
          <p>Grossery</p>
      </div>
      <div class="container-fluid">
          <div class="row">
              <div class="col-sm-3">
                <div class="filter_list">
                    <p @click="show = !show, rotate = !rotate">Category <i class="fa fa-angle-right" v-bind:class="{ rotate: rotate }"></i></p>
                    <transition-group name="slide-fade">
                        <ul v-if="show" v-for="list in lists" :key="list">
                            <li><a href="/">{{ list.prod }}</a></li> <!-- href must be follow to the current object, router should be help for this (:id)-->
                        </ul>
                    </transition-group>

                    <p @click="show1 = !show1, rotate1= !rotate1">Products <i class="fa fa-angle-right" v-bind:class="{ rotate1: rotate1 }"></i></p>
                    <transition-group name="slide-fade">
                        <ul v-if="show1" v-for="product in products" :key="product">
                            <li>{{ product.prod }}</li>
                        </ul>
                    </transition-group>
                </div>
              </div>

              <div class="col-sm-3">
                  <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                  <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                  <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>
              </div>

              <div class="col-sm-3">
                  <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                    <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                    <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>
              </div>
              <div class="col-sm-3">
                  <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                    <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>

                    <div class="coupon">
                    <div class="container">
                        <h3>Company Logo</h3>
                    </div>
                    <img src="src/assets/img/hamburger.jpg" alt="Avatar" style="width:100%;">
                    <div class="container" style="background-color:white">
                        <h2><b>20% OFF YOUR PURCHASE</b></h2> 
                        <p>Lorem ipsum..</p>
                    </div>
                    <div class="container">
                        <p>Use Promo Code: <span class="promo">BOH232</span></p>
                        <p class="expire">Expires: Jan 03, 2017</p>
                    </div>
                  </div>
              </div>
          </div>
      </div>
        <footer class='footer'>
            <span>20**</span>
        </footer>
  </div>
</template>

<script>

export default {
  name: "templates",
  data () {
      return {
          show: false,
          show1: false,
          rotate1: false,
          rotate: false,
          lists: [
              { prod: 'Product 1'},
              { prod: 'Product 2'},
              { prod: 'Product 3'},
              { prod: 'Product 4'},
              { prod: 'Product 5'},
              { prod: 'Product 6'},
              { prod: 'Product 7'},
              { prod: 'Product 8'},
          ],
          products: [
              { prod: 'Item 1'},
              { prod: 'Item 2'},
              { prod: 'Item 3'},
              { prod: 'Item 4'},
              { prod: 'Item 5'},
              { prod: 'Item 6'},
          ]
      }
  },
  mounted () {
     
  }, 
  methods: {
        
  }
}
</script>

<style scoped>


.catalog {
    text-align: center;
    font-size: 1.5em;
    padding: 20px;
}
.coupon {
    border: 1px solid #bbb;
    width: 100%; 
    border-radius: 15px; 
    margin: 30px auto;
    max-width: 600px;
    cursor: pointer;
    transition: .3s;
}

.coupon:hover {
    border: 1px solid #bbb; 
    width: 100%; 
    border-radius: 15px; 
    margin: 30px auto;
    max-width: 600px;
    cursor: pointer;
    box-shadow: 1px 1px 1px 1px rgba(0,0,0,.4);
    transition: .3s;
}

.container {
    padding: 12px 16px;
}

.promo {
    background: #ccc;
    padding: 2px;
}

.expire {
    padding: 5px 0 5px 0;
    color: red;
}

.filter_list {
    width: 100%;
    height: 100%;
    border-right: 1px solid gainsboro;
    transform: translateY(30px);
}


.filter_list p {
    text-align: left;
    font-size: 0.9em;
    cursor: pointer;
    padding: 0 0 0 10px;
    border-top: 1px solid gainsboro;
    border-bottom: 1px solid gainsboro;
}

.fa-angle-right {
    font-size: 1.1em;
    padding: 8px;
    transition: .3s;
}
.filter_list ul li {
    list-style-type: none;
    color: rgb(62,119,191);
    font-size: 0.8em;
    padding: 5px 5px 1px 20px;
}

.filter_list a {
    text-decoration: none;
    color: rgb(62,119,191);
    font-size: 0.8em;
    padding: 5px 5px 0 20px;
}

.rotate {
    transform: rotate(90deg);
    transition: .4s;
}

.rotate1 {
    transform: rotate(90deg);
    transition: .4s;
}


.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .2s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active до версии 2.1.8 */ {
  transform: translateX(-20px);
  opacity: 0;
}



.footer {
    position: relative;
    bottom: 0;
    width: 100%;
    height: 50px;
    background-color: rgba(71, 76, 78, 0.377);
}

.footer span {
  display: block;
  line-height: 3;
  text-align: center;
  color: rgb(52, 163, 238);
}
</style>
