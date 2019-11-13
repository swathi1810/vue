<template>
  <div class="card">
    <header class="card-header">
      <div class="Head">
        <div class="Heading">
          <p>Something</p>
          </div>
          <ulcomponent :items="items" :activeTab="activeTab" @changeTitle="changeTitle">
          </ulcomponent>
    </div>
    </header>
    <cardbody :subTab="activeTab" :items="items">
    </cardbody>
  </div>
</template>
<script>
import cardbody from './cardbody';
import ulcomponent from './ulcomponent';
export default{
  name:'TabCard',
  components:{
    ulcomponent,
    cardbody
  },
  props:{
    items:{
      type:Array,
      default:() =>[]
    }
  },
  data(){
return{
      activeTab:this.items[0].tabtitle
    };
  },
  methods:{
  changeTitle(tabName){
    this.activeTab=tabName;
  }
},
}
</script>
<style>
.Heading{
  padding-bottom: 90px;
  padding-top: 0px;
  position: relative;
}
.head{
  text-align: center;

}
p{
  font-size: 20px;
  font-family: fantasy;
}
.card {
  background-color: #fff;
  width: 680px;
  height: 1280px;
  border-radius: 6px;
  box-shadow: 2px 0px 30px 0 rgba(0, 0, 0, 0.14);
}

.card-header {
  background-color: #c95b0c;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  color: #fff;
  padding-top: 100px;
  padding-left: 170px;
  border-top-left-radius: 2px;
  border-top-right-radius: 2px;
  position: relative;
}

</style>
