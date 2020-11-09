<template>
  <div id="app">
    <Header :headCol = headerColor />
    <ColorPicker :colors="color" @setColor="setColor" />  
    <ColourGrid :color="headerColor" />
  </div>
</template>

<script>
import Header from '@/components/Header';
import ColorPicker from '@/components/ColorPicker';
import ColourGrid from '@/components/ColourGrid';
export default {
  name: 'App',
  components: {
    Header,
    ColorPicker,
    ColourGrid
  },
  data (){
    return{
      color: ["#000000","#333456","#52057b","#892cdc","#bc6ff1","#7579e7","#9ab3f5","#a3d8f4","#3797a4","#799351","#b8de6f","#b9fffc", "#ffdada","#f3bad6","#ea86b6","#e05297","#f05454","#af2d2d","#f6830f","#c56183"],
      headerColor : '#7579e7'
    }
  },
  methods :{
    setColor(color){
      this.headerColor = color;
    }
  }
}
</script>

<style>
body{
  margin: 0;
  background-color: #F3F3F3;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
