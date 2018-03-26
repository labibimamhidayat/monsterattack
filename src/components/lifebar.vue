<template>
  <el-col :span="12">
      <h2>{{label}}</h2>
      <div class="loading-background">
          <div :class="'loading-bar '+label" :style="'width : '+percentage+'%;'"></div>
          <div class="loading-number">
              {{percentage}} %
          </div>
      </div>
  </el-col>
</template>
<script>
    export default{
        props :{
            percentage: {
                type: Number,
                required: true
            },
            label : {
                type : String,
                required : true
            }
        },
        filters : {
            status(val){
                if(val == "monster"){
                    return "exception"
                }else{
                    return "success"
                }
            }
        }
    }
</script>
<style scoped>
    h2{
        text-align: center;
        margin-top: 0px;
        margin-bottom: 4px;
        text-transform: uppercase;
    }
    .loading-background{
        height: 20px;
        width: 100%;
        background: rgba(2, 16, 16, 0.5);
        position: relative;
        border-radius: 20px;
        overflow: hidden;
    }
    .loading-bar{
        height: 100%;
        border-radius: 20px;
        transition: width 0.5s linear
    }
    .player{
        background: #11998e;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #38ef7d, #11998e);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to right, #38ef7d, #11998e); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    }
    .monster{
        background: #8E0E00;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to bottom, #1F1C18, #8E0E00);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to bottom, #1F1C18, #8E0E00); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    }
    .loading-number{
        position: absolute;
        width: 100%;
        text-align: center;
        top : 1px;
        z-index: 20;
        color : yellow;
    }
</style>

