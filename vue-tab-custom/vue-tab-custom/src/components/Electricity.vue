<template>
  <div class="yo">
    <div class="me">
<img src="../assets/gryff.png" style="width:25px;height:25px">
 </div>
<TabCard :items="items">
</TabCard>
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
]
};
},
};
</script>
