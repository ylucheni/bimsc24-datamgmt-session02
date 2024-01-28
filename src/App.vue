<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()
let name = ref( "Yichen Lu" )
let count = ref(0)

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

<div id="sidebar" class="container"> <button @click="increment">Add one more</button></div>

<div id="sidebar" class="container"> <input type="text" v-model="inputText" />
    <button @click="addText">Add Text</button> </div>

    <div id="sidebar" class="container">{{ displayText }}</div>
      
<div id="main" class="container"> Count is: {{ count }}</div>

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

#navbar{

    height: 70px;
    border-color: red;


}

#flex{
    
    display: flex;
    height: calc(100vh - 70px);
}

#sidebar{
    
    width:20%;
    border-color: blue;

}

#main{
    width:80%;
    border-color: green;
    

}

#title{
    width: 70%;
    float:left;
}




.container{

    border-style: dotted;
    border-width: 1px;

}

button{
    margin-left: 10px;
}

</style>