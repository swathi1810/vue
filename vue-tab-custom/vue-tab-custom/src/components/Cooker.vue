<template>
<Insidecomponent :items="items">
</Insidecomponent>
</template>
<script>
import Insidecomponent from './Insidecomponent';
export default{
  name:'Cooker',
  components:{
    Insidecomponent,
  },
  data(){
    return{
      items:[
        {
          key:"acc",
          heading:'Account details',
          summary:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque aliquam orci ante, eu tincidunt erat ullamcorper quis. '
        },
        {
          key:"sum",
          heading:'Summary details',
          summary:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque aliquam orci ante, eu tincidunt erat ulla'
        },
        {
          key:"tot",
        heading:'Total savings made',
        summary:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque aliquam orci ante, eu tincidunt erat ulla'
      }

      ]
    }
  }
};
</script>
