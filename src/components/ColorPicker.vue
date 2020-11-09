<template>
<div class="color-picker">
    <div class = "color"
        v-for="(color,i) in colors"
        :key="i"
        :style=" 'background:'+color"
        @click="setColor(color)">
    </div>
</div>
    
</template>
<script>
export default {
    name: 'ColorPicker',
    props: ['colors'],
    methods:{
        setColor (color){
            this.$emit('setColor', color)
        }
    }
    
}
</script>
<style scoped>
.color-picker{
    width: 400px;
    display: grid;
    margin: 15px auto;
    grid-template-columns: repeat(20,25fr);

}
.color{
    border: 1px solid #000;
    height: 30px;
}

</style>