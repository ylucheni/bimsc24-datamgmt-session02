<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()
let name = ref( "Yichen Lu" )
let count = ref("0")

function increment() {
    count.value++;
}

</script>



<!-- the template is where the html code goes -->
<template>

<div id="navbar" class="container">  
        <div id="title">DATAMGMT - Assignment02</div>
        <div id="title">{{name}}</div>
</div>

<div id="flex">

        <div id="sidebar" class="container"> Sidebar </div>

        <button @click="increment">Add one more</button>

        <div id="main" class="container"> Text input </div>

</div>


</template>



<!-- style is where the css code goes -->
<style scoped>

div{
    
    background-color: rgb(0, 0, 0); 
    color: white;
}

body{

    margin:0;
}

div{

    /* put the borders in the inside of container */
    box-sizing: border-box;
}

img{

    height: 100%;
    width: auto;

}

#navbar{

    height: 70px;
    border-color: red;


}

#flex{
    
    display: flex;
    height: calc(100vh - 70px);
}

#sidebar{
    
    width:30%;
    border-color: blue;

}

#main{
    width:70%;
    border-color: green;

}

#title{
    width: 70%;
    float:left;
}

#logo{
    width: 30%;
    height: 100%;
    float:right;
    text-align: right;

}

.container{

    border-style: dotted;
    border-width: 1px;

}


</style>