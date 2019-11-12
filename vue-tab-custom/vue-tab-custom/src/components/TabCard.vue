<template>
  <div class="card">
    <header class="card-header">
      <div class="Head">
        <div class="Heading">
          <p>Something</p>
          </div>
      <ul class="tab-heads">
        <li
          class="tab-head"
          v-for="item in items"
          :key="item.key"
          v-bind:class="{
            'tab-head--active': activeTab === item.tabtitle
          }"
          v-on:click="switchTab(item.tabtitle);"
        >
        <div class="head">
        <div class="some">
          <div v-html="item.icon">
          </div>
        </div>
        <div class="right">
        {{item.tabtitle}}
      </div>
      </div>
</li>
      </ul>
    </div>
    </header>
    <main class="card-body">
      <div class="tab-panel">
        <template v-for="item in items" >
        <component :key="item.key" v-bind:is="item.component" v-show="activeTab===item.tabtitle">
        </component>
      </template>
      </div>
    </main>
  </div>
</template>
<script>
import Electricity from './Electricity';
import Gas from './Gas';
import Lilly from './Lilly';
import James from './James';
import Pressure from './Pressure';
import Cooker from './Cooker';
export default{
  Name:'TabCard',
  components:{
    Electricity,
    Gas,
    James,
    Lilly,
    Pressure,
    Cooker
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
  switchTab(tabName){
    this.activeTab=tabName;
  }
},
}
</script>
<style>
.tab-heads {
  display: flex;
  margin: 0;
  padding: 0;
  list-style: none;
  margin-left: 6px;
  margin-top: -4px;
  width: 700px;
  height: 60px;
}

.tab-head {
  width: 150px;
  padding-left:5px;
  padding-top: 18px;
  padding-right: 7px;
  border-top-left-radius: 2px;
  border-top-right-radius: 4px;
  position: relative;
  cursor: pointer;
  text-align: center;
}

.tab-head--active {
  background-color: #fff;
  color: #333;
  transition: 0.4s;
}

.card-body {
  padding: 20px 16px;
}
.Heading{
  padding-bottom: 90px;
  padding-top: 0px;
  position: relative;
}
.head{
  text-align: center;

}
.some{
  padding-bottom: -2px;
  padding-left: 18px;
  float: left;
}
.right{
  float: center;
  text-align: center;
  padding-bottom: -2px;
  padding-right: 25px;
}
p{
  font-size: 20px;
  font-family: fantasy;
}
.Heading{
  padding-bottom: 90px;
  padding-top: 0px;
  position: relative;
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
