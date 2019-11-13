<template>
    <TabCard :items="items">
    </TabCard>
</template>
<script>
import TabCard from './components/TabCard';
import Electricity from './components/Electricity';
import Gas from './components/Gas';
export default{
  name:'App',
  components:{
    TabCard,
  },
  data(){
    return{
     items:[
       {
         key:'elec',
         component:Electricity,
         tabtitle:'Electricity',
         icon:`<i class="fas fa-burn"></i>`
       },
       {
         key:'gas',
         component:Gas,
         tabtitle:'Gas',
         icon:`<i class="fas fa-angle-double-up"></i>`
       }
     ]
    };
  }
};
</script>
<style>
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  background-color: #eee;
  min-height: 100vh;
  display: grid;
  place-items: center;
  font-family: 'Roboto', sans-serif;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #0000;
}
</style>
