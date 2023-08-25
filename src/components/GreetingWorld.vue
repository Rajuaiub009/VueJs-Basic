<template>
<h1>Input Field</h1>
<input type="text" placeholder="name" v-model="name" /><br><br>
<input type="password" placeholder="Password" v-model="password" /><br><br>
<button @click="getData()">Get Value</button>

<h1>Get Checkbox and radio button value</h1>
<h2>Programming Language</h2>

<label for="C++">C++</label>
<input type="checkbox" value="C++" v-model="lang" id="C++" /><br>

<label for="java">Java</label>
<input type="checkbox" value="java" v-model="lang" id="java" /><br>

<label for="python">Python</label>
<input type="checkbox" value="python" v-model="lang" id="python" /><br>

<h3>Name of the Languages: {{ lang }}</h3>

<h2>Radio Button</h2>

<label for="python">Python</label>
<input type="radio" name="language" value="pyhton" v-model="languages" id="python" /><br>

<label for="vuejs">VueJs</label>
<input type="radio" name="language" value="vuejs" v-model="languages" id="vuejs" /><br>

<h3>Name of the Language:{{ languages }}</h3>

</template>

<script>
export default {
    name: 'GreetingWorld',

    data() {
        return {
            name: null,
            password: null,
            lang: [],
            languages: null
        }
    },

    methods: {
        getData() {
            console.warn("Details: ", this.name, this.password)
        }
    }

}
</script>
