<template>
  <el-row>
    <el-col :span="12" :offset="6" class="header">
        <h1>
            <slot></slot>
        </h1>
    </el-col>
  </el-row>
</template>
<script>
    
</script>
<style scoped>
    @import url('https://fonts.googleapis.com/css?family=IBM+Plex+Serif:300i,400i');
    .header{
        text-align: center;
        font-family: 'IBM Plex Serif', serif !important;
        font-size: 26px;
        text-shadow: 4px 4px 11px rgba(18, 173, 33, 0.91);
        color: #044404; 
    }
    .header > h1{
        margin-top: 0px;
        margin-bottom: 20px;
    }
</style>

