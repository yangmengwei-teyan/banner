<template>
  <div class="hello">
     我是子组
    <div class="box">
    <van-swipe :autoplay="3000">
  <van-swipe-item v-for="(image, index) in images" :key="index">
    <img style="width:100%" v-lazy="image" />
  </van-swipe-item>
</van-swipe>
     
      </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
     
       images: [
      'http://pica.nipic.com/2008-01-12/200811215275498_2.jpg',
      'http://pic24.nipic.com/20121029/3822951_090444696000_2.jpg',
      'https://img04.sogoucdn.com/app/a/100520093/ac75323d6b6de243-503c0c74be6ae02f-9a75e09210a0ab8ad2fcfb82ddac0ab4.jpg'
      ]
    };
  },
  
};
</script>


<style scoped>
.box {
  width: 100%;
  height: 200px;
  background: #ccc;
}
</style>
