<template>
  <div class="yo">
    <div class="me">
<img src="../assets/gryff.png" style="width:225px;height:225px">
 </div>
 <div class="geek">
  <TabCard :items="items" :show="show">
  </TabCard>
</div>
</div>
</template>
<script>
import TabCard from './TabCard';
import Pressure from './Pressure';
import Cooker from './Cooker';
export default{
  name:'Gas',
  components:{
    TabCard,
    Pressure,
    Cooker,
  },
  data(){
    return{
      items:[
        {
        key:'pre',
        component:Pressure,
        tabtitle:'Pressure',

      },
    {
      key:'cook',
  component:Cooker,
tabtitle:'Cooker'}
],
show:false
};
}
};
</script>
<style>
.yo{
  max-width: 980px;
  height: 1200px;
  position: relative;
}
.me{
  width: 300px;
  float: left;
  padding-top: 10px;
}
.geek{
  background-color: #fff;
  width: 590px;
  height: 800px;
  border-radius: 1px;
  border: 0;
  float:right;
}
</style>
