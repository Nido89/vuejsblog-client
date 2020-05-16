<template>
  <div id="app">
 <Header />
 <Latest />

  </div>
</template>

<script>
import Header from './components/Header';
import Latest from './components/Latest';

export default {
  name: 'App',
  components: {
    Header,
    Latest
  }
}
</script>

<style lang="scss">
body{
  background-color:lightgoldenrodyellow ;
  font-family: 'Times New Roman', Times, serif, Haettenschweiler, 'Arial Narrow Bold';

  h3{
    color: darkslategrey;
    font-size: 28px;
    font-weight: 700;
  }
}
</style>
