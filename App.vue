<template>
<div id="app">
    <p v-on:click="changeText"> {{message}} </p>
    <ul>
        <li v-for="fruit in fruits" 
        v-bind:key="fruit"
        v-on:click="addFruit(fruit)"
        >{{fruit.text}}</li>
    </ul>
</div> 
</template>

<script>
export default {
    data: () => ({
        message: "Fruit!",
        fruits: [
            {text:"Banana"},
            {text:"Kiwi"}, 
            {text:"Carrot"},
            {text:"Orange"},
            {text:"Apple"}        
        ],
        sallad : []
    }),

    methods: {
        changeText(){            
            this.message = "GrillKorv"
        }
    }
}
</script>

<!--<style>
#app{
    background-color: hotpink;
}
</style>-->