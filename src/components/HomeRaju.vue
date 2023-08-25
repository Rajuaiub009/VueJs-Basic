<template>
<h2>Welcome to Home Page</h2>

<h1 v-on:mousemove="dataConsole()">Raju Component</h1>
<button @click="clickMe()">Click Me</button> <br> <br>
<button @click="clickMeNow('Its Working')">Click Me Now</button>
<button @dblclick="doubleClickMe('Double click Working')">Double Click</button>
<button @click="increment">Increment</button>
<h3>{{ count }}</h3>

<h3>Total price is {{ 50 + 50 }} Taka</h3>
<h3>Email: {{ email }} </h3>
<h3>Profession: {{ profession }}</h3>
<h3>Country: {{ country }}</h3>
<h3>Name: {{ getInfo("Raju") }}</h3>
<h2>{{ getData().email}}</h2>
</template>

<script>
import {
    ref
} from 'vue';
export default {
    name: "HomeRaju",

    data() {
        return {
            email: 'raju@gmail.com',
            profession: 'Student',
            country: 'Bangladesh',
        }
    },

    setup() {
        const count = ref(0);
        const increment = () => {
            count.value++;

        };
        return{
            count,
            increment
        };
    },

    methods: {
        getInfo(info) {
            return info;
        },

        clickMe() {
            alert("it is working")
        },

        clickMeNow(name) {
            alert(name)

        },

        doubleClickMe(name) {
            alert(name)
        },
        dataConsole() {
            console.warn("Its working in Console")
        },
        getData() {
            return {

                email: this.email
            }
        }
    }
}
</script>
