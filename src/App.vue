<template>
  <div id="app" class="container">
    <a href="#" id="a-lang">English</a>
    <header id="header">
      <div class="header-content row">
        <div class="header-content-text col-md-6 col-lg-6 col-xs-12 col-sm-12">
          <h1>你好，</h1>
          <h2>我是Robin</h2>
          <p>在学习中的一名小码农</p>
          <p>少即是多是我的主义</p>
          <a href="https://github.com/675076143">GitHub</a><br/>
          <a href="https://blog.csdn.net/Robin_John">Blog</a>
        </div>
        <div class="header-content-img col-md-6 col-lg-6 col-xs-12 col-sm-12">
          <img src="./assets/Robin.jpg" alt="Robin" class="img-fluid">
        </div>
      </div>

    </header>
    <main class="main">
      <article class="hobby">
        <h1 class="hobby-header">我喜欢</h1>
        <section class="hobby-body">
          <div class="row no-gutters hobby-item">
            <div class="col-4">
              <img src="./assets/visual_game_boy_96px.png" class="card-img" alt="...">
            </div>
            <div class="col-8">
              <div class="card-body">
                <h5 class="card-title">游戏</h5>
                <p class="card-text">人菜，但爱玩</p>
                <a href="https://steamcommunity.com/profiles/76561198087530886/" class="card-text"><small class="text-muted">我的Steam主页</small></a>
              </div>
            </div>
          </div>
          <div class="row no-gutters hobby-item">
            <div class="col-8">
              <div class="card-body">
                <h5 class="card-title">音乐</h5>
                <p class="card-text">不会，但爱听</p>
                <p class="card-text"><small class="text-muted">网易云ID: Robin_John</small></p>
              </div>
            </div>
            <div class="col-4">
              <img src="./assets/music_96px.png" class="card-img" alt="...">
            </div>
          </div>
          <div class="row no-gutters hobby-item">
            <div class="col-4">
              <img src="./assets/regular_biking_96px.png" class="card-img" alt="...">
            </div>
            <div class="col-8">
              <div class="card-body">
                <h5 class="card-title">运动</h5>
                <p class="card-text">武术：“再来一组”</p>
                <p class="card-text">骑行：“最后一圈” “拐个弯就到了”</p>
              </div>
            </div>
          </div>
        </section>
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
p{
  margin-bottom: 0!important;
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
  height: 100%;
}
#header{
  height: 100%;
  overflow: hidden;
  display: flex;
  align-items: center;
  h1{
  }
  h2{
    margin-left: 10px;
    position: relative;
    z-index: 99;
    text-shadow: 5px 5px 20px #f6f6f6;
  }
  p{
    margin: 0 0 0 20px;
  }
  img{
    box-shadow: 10px 10px 10px rgba(0,0,0,0.6);
  }
}
article{
  height: 100%;
}
.hobby-header{
  margin-bottom: 40px
}
.hobby-item{
  margin:20px;
  background-color: #f4f4f4;
  /*opacity: 0;*/
  transition: all 0.2s;
}
.hobby-item:nth-child(1){
  border-right: 10px solid rgb(50,62,86);
}
  .hobby-item:nth-child(2){
    border-left: 10px solid indianred;
  }
  .hobby-item:nth-child(3){
    border-right: 10px solid black;
  }
</style>
<script>
  const resizeFont = ()=>{
    const {clientWidth} = document.documentElement
    if(clientWidth>=960){
      document.documentElement.style.fontSize = 960/30+'px'
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
  window.onscroll = ()=>{
    //头部滚动显示与隐藏
    const headerText = document.querySelector(".header-content-text")
    const headerImg = document.querySelector(".header-content-img")
    // const header = document.querySelector("header")
    //获取滚动位置
    const {scrollTop} = document.documentElement
    // console.log("scroll")
    headerText.style.transform = `translate(-${scrollTop}px,0px)`
    headerText.style.opacity = 20/scrollTop;
    headerImg.style.transform = `translate(${scrollTop}px,0px)`
    headerImg.style.opacity = 20/scrollTop
    // const hobbyHeader = document.querySelector(".hobby-header")
    // const hobbyItem = document.querySelector('.hobby-item')
    //滚动到能看到Header的时候开始进入
    // if(hobbyHeader.offsetTop - scrollTop< document.documentElement.clientHeight/2)
    // hobbyItem.style.transform = `translate(${scrollTop}px,0px)`

  }
</script>