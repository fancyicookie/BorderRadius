<!--
 * @Date: 2022-11-17 15:13:55
 * @Author: Fancyicookie
-->
<template>
<div class="all">
  <div 
  class="box" 
  :style="{ 
    'border-top-left-radius': top_left_val + 'px',
    'border-top-right-radius': top_right_val + 'px',
    'border-bottom-left-radius': bottom_left_val + 'px',
    'border-bottom-right-radius': bottom_right_val + 'px',
    }"
  >
  <input type="text" class="tl" v-model.trim="tl_value" />
  <input type="text" class="tr" v-model.trim="tr_value" />
  <input type="text" class="br" v-model.trim="br_value" />
  <input type="text" class="bl" v-model.trim="bl_value" />
  </div>

  <!-- <div class="box" style="border-radius: 20% 80% 70% 30% / 21% 90% 10% 79% "></div> -->
  
  <div class="content">border-radius: {{ tl_value }}px {{ tr_value }}px {{ br_value }}px {{ bl_value }}px;</div>
  <!-- <el-switch class="switch" v-model="value1" active-text="Width: 200px; Height: 200px" inactive-text="Custom Size"></el-switch> -->
</div>
</template>

<script>
export default {
    data() {
        return {
            tl_value: 0,
            tr_value: 0,
            bl_value: 0,
            br_value: 0,
            value1: true
        }
    },
    computed: {
        top_left_val() {
            return this.tl_value
        },
        top_right_val() {
            return this.tr_value
        },
        bottom_left_val() {
            return this.bl_value
        },
        bottom_right_val() {
            return this.br_value
        }
    }
}
</script>

<style>
.box {
    position: relative;
    margin: 60px auto;
    width: 200px;
    height: 200px;
    background-image:linear-gradient(rgb(149, 0, 255),rgb(45, 0, 128));
    text-align: center;
}
input {
    position: absolute;
    display: block;
    margin: 0px auto;
}
.tl {
    width: 30px;
    margin: -20px -50px;
}
.tr {
    width: 30px;
    margin: -20px 215px;
}
.br {
    width: 30px;
    margin: 200px 215px;
}
.bl {
    width: 30px;
    margin: 200px -50px;
}
.content {
    font-family: Verdana, sans-serif;
    font-size: 20px;
}
.switch {
    margin-top: 20px;
}
</style>