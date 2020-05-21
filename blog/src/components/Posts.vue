<template>
  <div class="posts">
      <div class="post" v-for="post in posts.slice(6,count)" :key="post._id">
          <h3>{{ post.title }}</h3>
      </div>
      <button class="load" @click="$emit('showMore')" v-if="count < posts.length">View More</button>
  </div>
</template>

<script>
export default {
    name: 'posts',
    props: ['posts','count']
}
</script>

<style lang="scss" scoped>
.posts{
    width: 100%;
    max-width: 1280px;
    .post{
        display: block;
        padding: 15px;
        background: lightcyan;
        box-shadow: 3px 3px 8px 0px rgba($color: #000000, $alpha: 1.0);
        margin-bottom: 15px;
    }


    margin: 50px auto;
    .load{
        display: block;
        width: 100%;
        max-width: 250px;
        height: 50px;

        margin: 0 auto;

        outline: none;
        border: double;

        border-radius: 25px;
        appearance: none;
        background-color: darkturquoise;
        box-shadow: 3px 3px 8px 0px rgba($color: #000000, $alpha: 1.0);

        color: yellow;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        font-size: 28px;

        box-sizing: border-box;
    }
}

</style>