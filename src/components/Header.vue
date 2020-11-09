<template>
    <header>
        <h3>Grid<span>ker</span></h3>
        <p>A simple grid colour picker field made with Vue.js</p>
        <div class="color" :style=" 'background:'+headCol"></div>
       
    </header>
</template>
<script>
export default {
    name: 'Header',
    props:['headCol']
}
</script>
<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100px;
    background-color: black ;
    padding: 0px 15px;
}
h3{
    color: #19d3daec;
    font-size: 40px;
    font-weight: 600;
    text-transform: uppercase;
}
h3 span{
    color: #FFCE00;
    font-weight: 900;
}
.color{
    border: 3px dashed #f3f3f3;
    height: 70px;
    width: 70px;

}
p{
    text-align: center;
}
</style>