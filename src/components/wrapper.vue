<template>
    <el-row :gutter="30">
        <el-col :span="16" :offset="4" class="wrapper">
            <slot></slot>
        </el-col>
    </el-row>
</template>
<script>
    
</script>

<style scoped>
    .wrapper{
        border-radius: 10px;
        background-color: rgba(255,255,255,0.5);
        padding-bottom: 15px;
        padding-top: 15px;
    }
</style>


