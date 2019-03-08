<template>
  

    <div :style="{backgroundColor:bgColor}">
    <button @click="Start"> Start/Stop</button>
      HelloWorhddhld
    </div>

</template>

<script> 
function Random(max){
  return Math.floor(Math.random() * Math.floor(max));
}
export default {
  
  data(){
    return{
      bgColor:'yellow',
      color:["orange","green","pink","blue","grey"],
      timer:null,
    };
  },
  methods:{
    change(){
      this.bgColor=this.color[Random(5)];
    }
  Start(){
    if (this.timer){
      clearInterval(this.timer);
    }
    this.timer = setInterval(this.change,30) 
  }
  }
}
</script>

<style>
  div{
    position:fixed;
    top:0;
    bottom:0;
    right:0; 
    left:0;
  }
</style>