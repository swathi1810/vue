<template >
  <div>
    <div v-for="item in items" :key="item.key">
      <div class="details">
      <div class="sub">
      {{item.heading}}
    </div>
    <div class="desc">
      {{item.summary}}
    </div>
  </div>
  </div>
  </div>
</template>
<script>
export default{
  name:'Insidecomponent',
  props:{
    items:{
      type:Array
    }
  }
};
</script>
<style>
.details{
  position: relative;
  margin-top: 20px;
}
.details::after{
  content:'';
  position:absolute;
  background-color: #65a9b5;
  width: 90%;
  height: 3px;
  bottom: -15px;
  left:0;
}
.sub{
  margin-bottom: 20px;
  padding-top: 20px;
  font-weight: bold;
  color: #65a9b5;
  font-size: 20px;
}
.desc{
  margin-bottom: 20px;
}
</style>
