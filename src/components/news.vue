<template>
  <div class="news">
    <div class="container-fluid">
        <div class="row news_main">
            <div class="col-sm-9">
                <h2>News</h2>                  
                <h3>{{ msg }}<br><br>{{ msg }}<br><br>{{ msg }}<br><br>{{ msg }}<br><br>{{ msg }}<br><br>{{ msg }}<br><br>{{ msg }}</h3>
            </div>
            <div class="col-sm-3">
                <div class="inner_content">
                    <h2>Latest news</h2>
                    <p>{{ msg }}{{ msg }}{{ msg }}</p>

                    <h2>Latest news</h2>
                    <p>{{ msg }}{{ msg }}{{ msg }}</p>

                </div>
                
            </div>
        </div>
    </div>
        <section class="news_second_section parallax-window" data-parallax="scroll" data-image-src="/src/assets/img/landscape.jpg">
            <img src="src/assets/img/landscape.jpg" alt="">
        </section>
    <div class="text_container">
        <p>{{ msg }}</p>
    </div>
    <footer class='footer'>
        <span>20**</span>
    </footer>
  </div>
</template>

<script>

export default {
  name: "news",
  data () {
      return {
          msg: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis dignissimos illo ipsam exercitationem, esse, ut voluptatibus ad laborum debitis voluptates deleniti, assumenda neque facilis hic nesciunt animi odit quasi! Alias!Nobis quia corporis officia labore cumque praesentium, consequuntur ipsam pariatur quos. Perferendis magni dolorem consequatur nemo consectetur adipisci sint similique minima? Ex nobis eligendi ea temporibus veniam cum sunt est.'
      }
  },
  mounted() {
      
  },
  methods: {
      test() {
          console.log('test')
      }
  }
}
</script>

<style lang="scss">

.news {
    position: relative;
    padding: 10px 0 0 0;
    overflow-x: hidden;
    width: 100%;
    min-height: 100%;
    background-color: rgb(255, 255, 255);

}

.news_main {
    width: 100%;
    height: 100%;
    position: relative;
    margin: 0 auto;
}

.news_main h3 {
    text-align: center;
    font-size: 1.1em;
    padding: 10px;
    height: 100%;
    font-weight: normal;
    position: relative;
}

.inner_content {
    position: relative;
    display: block;
    height: 100%;
    border-left: 1px solid gainsboro;
}

.inner_content p {
    position: relative;
    display: block;
    text-align: center;
    font-size: 1.1em;
    padding: 10px;
    max-height: 300px;
    max-width: 300px;
    overflow-y: scroll;
    overflow-x: hidden;
    margin: 0 auto;
}


.parallax-window {
  min-height: 320px;
  background: transparent;

}


.news_main h2{
    font-weight: bolder;
    font-size: 1.2em;
    text-align: center;
    padding: 20px 0 5px 0;

}
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

.news_second_section {
    position: relative;
    width: 100%;
    height: 40vh;
}

.news_second_section img {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 20px 0 10px 0;
}

.text_container {
    width: 100%;
    height: 100%;
    padding: 10px 30px 20px 30px;
    margin: 0 auto;
    font-size: 1.7em;
    text-align: center;
}

@media (max-width: 576px){
    .inner_content {
    position: relative;
    display: block;
    height: 100%;
    border: none;
}
}

</style>


