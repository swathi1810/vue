<template>
  <div class="yo">
    <div class="me">
<img src="../assets/gryff.png" style="width:225px;height:225px">
 </div>
 <div class="geek">
<TabCard :items="items" :show="show" >
</TabCard>
</div>
</div>
</template>
<script>
import TabCard from './TabCard';
import James from './James';
import Lilly from './Lilly';
export default{
  name:'Electricity',
  components:{
    TabCard,
    James,
    Lilly,
  },
  data(){
    return{
      items:[
        {
        key:'lil',
        component:Lilly,
        tabtitle:'Lilly',

      },
    {
      key:'jam',
  component:James,
tabtitle:'James'}
],
show:false
};
},
};
</script>
<style>
.yo{
  max-width: 980px;
  height: 1200px;
  position: relative;
}
.me{
  width: 380px;
  float: left;
  padding-top: 10px;
}
.geek{
  background-color: #6d32a8;
  width: 590px;
  height: 800px;
  border-radius: 1px;
  float: right;
  border:0;
  padding-left: 0px;

}
</style>
