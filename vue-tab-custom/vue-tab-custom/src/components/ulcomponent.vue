<template>
  <ul class="tab-heads">
    <li
      class="tab-head"
      v-for="item in items"
      :key="item.key"
      v-bind:class="{
        'tab-head--active': activeTab === item.tabtitle
      }"
      v-on:click="changeTitle(item.tabtitle)"
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
</template>
<script>
export default{
  name:'ulcomponent',
  props:{
    items:Array,
    activeTab:String
  },
  methods:{
    changeTitle:function(tabtitle){
      this.$emit('changeTitle',tabtitle);
    }
  }
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
</style>
