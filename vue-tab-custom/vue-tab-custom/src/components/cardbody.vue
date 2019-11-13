<template>
  <main class="card-body">
    <div class="tab-panel">
      <template v-for="item in items" >
      <component :key="item.key" v-bind:is="item.component" v-show="subTab===item.tabtitle">
      </component>
    </template>
    </div>
  </main>
</template>
<script>
import Gas from './Gas';
import Electricity from './Electricity';
export default{
  name:'cardbody',
  compoents:{
    Electricity,
    Gas
  },
  props:{
    subTab:String,
    items:Array
  },
};
</script>
<style>
.card-body {
  padding: 20px 16px;
}
</style>
