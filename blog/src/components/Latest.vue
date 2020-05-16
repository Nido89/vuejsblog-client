<template>
  <section class="latest">
    <h2>Most Recent Posts</h2>
    <div class="posts">
        <div class="post">
            <div class="image" :style="{backgroundImage:`url(${require('../assets/ReactAvatarsApi.png')})`}"></div>
            <h4>ReactJs-Api Usage</h4>
        </div>
        <div class="post col-2 row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/MasterThesisRobots.png')})`}"></div>
            <h4>Robotics and MachineLearning</h4>
        </div>
        <div class="post row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/JsVirtualAssistant.png')})`}"></div>
            <h4>A.I Virtual Assistant</h4>
        </div>
        <div class="post row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/VanilaJsNewsApp.png')})`}"></div>
            <h4>Vanilla Js Api</h4>
        </div>
        <div class="post">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/AI-Facial.png')})`}"></div>
            <h4>Facial Data with A.I</h4>
        </div>
        <div class="post col-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/djangoecom.png')})`}"></div>
            <h4>Django-Framework</h4>
        </div>
          <div class="post row-3">
                <div class="image" :style="{backgroundImage:`url(${require('../assets/SnakeGame.png')})`}"></div>
            <h4>Games with JS</h4>
        </div>
         <div class="post row-3">
               <div class="image" :style="{backgroundImage:`url(${require('../assets/LAMPStack-Chatapp.png')})`}"></div>
            <h4>LAMP Stack-RealtimeChats</h4>
        </div>
         <div class="post row-3">
               <div class="image" :style="{backgroundImage:`url(${require('../assets/Mevnstackchatapp.png')})`}"></div>
            <h4>MEVN Stack Power of Vue</h4>
        </div>
        <div class="post row-3">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/coronagame.png')})`}"></div>
            <h4>Humans vs Corona</h4>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name:'latest'
}
</script>

<style lang="scss" scoped>
.latest{
    display: block;
    width: 100%;
    max-width: 1280px;
    margin: 0 auto;

    .posts{
        display: grid;
        grid-template-columns: repeat(4,1fr);
        grid-template-rows: repeat(4,296px);
        grid-gap: 30px;

        margin: 15px;

        .post{
            display: flex;
            flex-direction: column;
            background-color: aliceblue;
            box-shadow: 3px 3px 8px 0px rgba($color: #000000, $alpha: 1.0);
            
            .image{
                flex: 1;
                background-position: center;
                background-size: cover;
                background-repeat: no-repeat;
            }
            
            h4{
                box-sizing: border-box;
                padding: 3px 15px 0px 15px;
                height: 50px;
                line-height: 50px;
                margin: 0px;

            }
            &.col-2{
                grid-column: span 2;
            }
            &.row-2{
                grid-row: span 2;
            }

        }
    }
}
</style>