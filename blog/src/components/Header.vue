<template>
  <header>
      <div class="left">
          <img src="../assets/logo.png" alt="JN" 
          class="logo"></div>
          <div class="center">
              <div class="title">
                  <h3 class="top">What'sIn</h3>
                  <h1>Jalal Naveed's</h1>
                  <h3>Brain</h3>
              </div>
          </div>

          <div class="right">
              
              <label for="search-bar">
                   <i class=" icon fas fa-search"></i>  <input type="text" name="search-bar" placeholder="Search Cool Stuff here..." id="search-bar">
              </label> 
          </div>           
  </header> 
</template>

<script>

export default {
    name: 'header'
}
</script>

<style lang="scss" scoped>
@import url("https://use.fontawesome.com/releases/v5.6.3/css/all.css");
header{
    display: flex;
    justify-content: center;
    padding: 50px 50px 0px;
    .left{
        flex: 1;
        .logo{
                width: 100px;
                height: 100px;
                border-radius: 55%;
                border-color: teal;
                border-style: dotted;
            }
    }
    .center{
        h3{
            font-size: 32px;
            font-style: italic;
            font-weight: 500;
            margin: 0;

            &.bottom{
                text-align: right;
            }
        }
        h1{
            color: dodgerblue;
            font-size: 72px;
            margin: 0;

        }
    }
    .right{
        flex: 1;
        display: flex;
        justify-content: flex-end;
        label{
            position: relative;
            display: block;
            width: 300px;
           
            input{
                width: 100%;
                height: 23px;
                background-color: lightcyan;
                box-shadow: 2px 2px 8px 0px rgba($color: #000000, $alpha: 1.0);
                margin: 0;
                padding: 5px 0px 0px 35px;
                box-sizing: border-box;
                appearance: none;
                border: double;
                border-radius: 15px;
                outline: none;
                color: green;
                font-family: Arial, fantasy, sans-serif;
                font-size: 16px;
                &::placeholder{
                    color: teal;
                }

            }
            .icon{
                position: absolute;
                width: 25px;
                height: 35px;
                margin: 5px;
            }
        }
    }
}

</style>