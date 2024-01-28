<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()
let name = ref( "Yichen Lu" )
let count = ref(0)

function increment() {
count.value++;
}


const inputText = ref('');
const displayText = ref('');

const addText = () => {
displayText.value = inputText.value;
}



</script>



<!-- the template is where the html code goes -->
<template>

<div id="navbar" class="container">  
        <div id="title">DATAMGMT - Assignment02</div>
        <div id="title">{{name}}</div>
</div>

<div id="flex">

<div id="sidebar" class="container"> <P> column 1_conout number </P><button @click="increment">Add one more</button> Count is: {{ count }} </div>

<div id="sidebar" class="container"> 
    <P> column 2_adding text </P>
    <button @click="addText">Add Text</button> 
    <input type="text" v-model="inputText" />
    <p>{{ displayText }}</p>
</div>

<div id="main" class="container"> <p>mian</p> </div>



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
    
    width:18%;
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