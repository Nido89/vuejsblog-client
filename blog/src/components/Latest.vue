<template>
  <section class="latest">
    <h2>Most Recent Posts</h2>
    <div class="posts" v-if="posts.length >=6">
        <div class="post">
            <div class="image" :style="{backgroundImage:`url(${require('../assets/ReactAvatarsApi.png')})`}"></div>
            <h4 :title="posts[1].title">{{posts[1].title}}</h4>
        </div>
        <div class="post col-2 row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/MasterThesisRobots.png')})`}"></div>
            <h4 :title="posts[0].title">{{posts[0].title}}</h4>
        </div>
        <div class="post row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/JsVirtualAssistant.png')})`}"></div>
             <h4 :title="posts[2].title">{{posts[2].title}}</h4>
        </div>
        <div class="post row-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/VanilaJsNewsApp.png')})`}"></div>
             <h4 :title="posts[3].title">{{posts[3].title}}</h4>
        </div>
        <div class="post">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/AI-Facial.png')})`}"></div>
             <h4 :title="posts[4].title">{{posts[4].title}}</h4>
        </div>
        <div class="post col-2">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/djangoecom.png')})`}"></div>
            <h4 :title="posts[5].title">{{posts[5].title}}</h4>
        </div>
          <div class="post row-3">
                <div class="image" :style="{backgroundImage:`url(${require('../assets/SnakeGame.png')})`}"></div>
            <h4 :title="posts[6].title">{{posts[6].title}}</h4>
        </div>
         <div class="post row-3">
               <div class="image" :style="{backgroundImage:`url(${require('../assets/LAMPStack-Chatapp.png')})`}"></div>
            <h4 :title="posts[7].title">{{posts[7].title}}</h4>
        </div>
         <div class="post row-3">
               <div class="image" :style="{backgroundImage:`url(${require('../assets/Mevnstackchatapp.png')})`}"></div>
             <h4 :title="posts[8].title">{{posts[8].title}}</h4>
        </div>
        <div class="post row-3">
              <div class="image" :style="{backgroundImage:`url(${require('../assets/coronagame.png')})`}"></div>
            <h4 :title="posts[9].title">{{posts[9].title}}</h4>
        </div>
    </div>
    <div class="posts" v-else>
        <p>Not enough posts to display</p>
    </div>
  </section>
</template>

<script>
export default {
    name:'latest',
    props: ['posts']
}
</script>

<style lang="scss" scoped>
.latest{
    display: block;
    width: 100%;
    max-width: 1280px;
    margin: 0 auto;
    h2{
        color: darkslateblue;
    }

    .posts{
        display: grid;
        grid-template-columns: repeat(4,1fr);
        grid-template-rows: repeat(4,296px);
        grid-gap: 30px;
        border: none;

        margin: 15px;

        .post{
            display: flex;
            flex-direction: column;
            background-color: lightskyblue;
            box-shadow: 3px 3px 8px 0px rgba($color: #000000, $alpha: 1.0);
            border-radius: 45px;
            
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
                overflow: hidden;
                color: yellow;
                font-size: 22px;
                font-weight: 500;
                text-overflow: hidden;

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