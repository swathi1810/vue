<template>
  <ul v-bind:class="{'tab-heads':show,'tab-heads1':!show}">
    <li
      class="tab-head"
      v-for="item in items"
      :key="item.key"
      v-bind:class="{'tab-head--active':activeTab===item.tabtitle && show,'tab-head--active1': activeTab===item.tabtitle && !show}"
      v-on:click="changeTitle(item.tabtitle)"
    >
    <div v-bind:class="{'head':show,'head1':!show}">
    <div class="left-icon">
      <div v-html='item.icon'>
      </div>
    </div>
    <div class="right-title">
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
    activeTab:String,
    show:Boolean
  },
  data(){
    return {getMe:this.show};
  },
  methods:{
    changeTitle:function(tabtitle){
      this.$emit('changeTitle',tabtitle);
    },
  }
};
</script>
<style>
.tab-heads {
  display: flex;
  margin: 0;
  padding: 0;
  list-style: none;
  margin-left: 9px;
  margin-top: -4px;
  max-width: 200px;
  max-height: 100px;
}
.tab-heads1{
  display: flex;
  list-style: none;
  margin-left: 6px;
  margin-top: -4px;
  max-width: 200px;
  max-height: 60px;
  position: relative;
}
.tab-heads1::after{
  content: '';
  position: absolute;
  background-color: #d7d9de;
  width: 130%;
  height:3px;
  bottom: -7px;
  left: 0;
}
.tab-head {
  max-width: 150px;
  padding-left:5px;
  padding-top: 18px;
  padding-right: 7px;
  border-top-left-radius: 2px;
  border-top-right-radius: 4px;
  position: relative;
  cursor: pointer;
  text-align: center;
  width: 150px;
}

.tab-head--active {
  background-color: #fff;
  color: #032270;
  transition: 0.4s;
}
.tab-head--active1{
  margin-top: -4px;
  background-color: #fff;
  color: #032270;
  transition: 0.4s;
  position: relative;
}
.tab-head--active1::after{
  content:'';
  position:absolute;
  background-color: #032270;
  width: 70%;
  height: 3px;
  bottom: -7px;
  left:0;
  z-index: 99999;
}
.left-icon{
  padding-bottom: 0px;
  padding-left: 18px;
  float: left;
  margin-right: 8px;
  z-index: 999999
}
.right-title{
  float: right;
  text-align: center;
  padding-bottom: -2px;
  padding-right: 25px;
}
.head{
  padding-left: 3px;
  padding-bottom: 10px;
  display: flex;
}
.head1{
   padding-left: 8px;
}
</style>
