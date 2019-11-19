<template>
  <div>
    <header v-bind:class="changeHeader">
      <div class="Head">
        <div v-if="show" class="Heading">
          <h2>HOW TO READ YOUR BILL</h2>
          <p> Blah blah ...blah</p>
          </div>
          <ulcomponent :items="items" :activeTab="activeTab" @changeTitle="changeTitle" :show="show">
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
    cardbody,
  },
  props:{
    items:{
      type:Array,
      default:() =>[]
    },
    show:{
      type:Boolean
    }
  },
  data(){
return{
      activeTab:this.items[0].tabtitle,
      getMe:this.show
    };
  },
  methods:{
  changeTitle(tabName){
    this.activeTab=tabName;
  }
},
computed:{
  changeHeader:function(){
    return this.getMe ? 'card-header' : 'card-header1';
  }
}
};
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

.card-header {
  background-color: #3d0212;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  color: #fff;
  padding-top: 100px;
  padding-left: 270px;
  border-top-left-radius: 2px;
  border-top-right-radius: 2px;
  position: relative;
}

.card-header1{
  background-color: #fff;
}

</style>
