<template>
  <div class="card">
    <TabCard :items="items" :show="show">
    </TabCard>
  </div>
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
         icon:'<i class="far fa-lightbulb"></i>'
       },
       {
         key:'gas',
         component:Gas,
         tabtitle:'Gas',
         icon:'<i class="fas fa-burn"></i>'
       }
     ],
     show:true
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
.card {
  background-color: #fff;
  width: 980px;
  height: 1280px;
  border-radius: 6px;
  box-shadow: 2px 0px 30px 0 rgba(0, 0, 0, 0.14);
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #0000;
}
</style>
