<template>
  <div id="overlay">
    <div class="content">
      <img :src="val.src" />
      <p @click="$emit('close')" class="close-btn">×</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeModal',
  props: ['val'],
}
</script>

<style scoped>
#overlay{
  z-index:1;
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background-color:rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center;
  justify-content: center;
}
.content{
  z-index:2;
  width:45%;
  padding-top: 5em;
  padding-bottom: 5em;
  text-align: center;
}
.content img {
  width: 60%;
}
.close-btn {
  color: #fff;
  font-size: 50px;
  position: absolute; 
  right: 30%;
  top: 0;
  cursor: pointer;
}

@media screen and (max-width: 767px) {
  .content {
    width: 60%;
  }
  .content img {
    width: 100%;
  }
  .close-btn {
  position: absolute; 
  right: 15%;
  top: 0%;
  cursor: pointer;
  }
}
</style>