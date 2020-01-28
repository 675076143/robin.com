<template>
  <div id="app" class="container">
    <a href="#" id="a-lang">English</a>
    <header id="header" class="row center-block">
      <div class="text col-md-6 col-lg-6 col-xs-12 col-sm-12">
        <h1>你好，</h1>
        <h2>我是Robin</h2>
        <p>在学习中的一名小码农</p>
        <p>少即是多是我的主义</p>
      </div>
      <div class="col-md-6 col-lg-6 col-xs-12 col-sm-12">
        <img src="./assets/Robin.jpg" alt="Robin" class="img-fluid">
      </div>

    </header>
    <main class="main">
      <article>
      </article>
    </main>
  </div>
</template>

<style lang="less">
  /*color:#404040*/
*{
  font-family: Consolas;
  color: #404040;
}
html,body{
  width: 100%;
  height: 100%;
}
#a-lang{
  position: fixed;
  top: 0;
  right: 10px;
  font-size: 1px;
}
#app{
  display: flex;
  width: 100%;
  height: 100%;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
#header{
  margin: 0 auto;
  h1{
    margin-left: -20px;
  }
  h2{
    margin-left: -10px;
    position: relative;
    z-index: 99;
    text-shadow: 5px 5px 20px #f6f6f6;
  }
  p{
    margin: 1px;
  }
  img{
    box-shadow: 10px 10px 10px rgba(0,0,0,0.6);
  }
}

</style>
<script>
  const resizeFont = ()=>{
    const {clientWidth} = document.documentElement
    if(clientWidth>=1080){
      document.documentElement.style.fontSize = 1080/30+'px'
    }else if(document.documentElement.clientWidth<=360){
      document.documentElement.style.fontSize = 360/30+'px'
    }else {
      document.documentElement.style.fontSize = clientWidth/30+'px'
    }
  }
  resizeFont()
  window.onresize = ()=>{
    resizeFont()
  }

  export  default {
    mounted() {

    },
    methods:{

    }
  }
</script>