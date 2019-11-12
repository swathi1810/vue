<template>
  <div class="yo">
    <div class="me">
<img src="../assets/gryff.png" style="width:25px;height:25px">
<p>Something</p>
 </div>
  <TabCard :items="items">
  </TabCard>
</div>
</template>

<script>
import TabCard from './TabCard';
import Pressure from './Pressure';
import Cooker from './Cooker';
export default{
  Name:'Gas',
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
        tabtitle:'Pressure',},
    {
      key:'jam',
  component:Cooker,
tabtitle:'Cooker'}]
};
}
};
</script>
