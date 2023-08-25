<template>
<h1 v-if="msg">If-Else Condition</h1>
<button @click="msg=1">Show</button>
<button @click="msg=0">Hide</button>

<h1>For Loop</h1>
<ul>
    <li v-for="item in technology" :key="item">{{ item }}</li>
</ul>

<h1>Array of Object</h1>
<ul>
    <li v-for="item in profiles" :key="item.age">Name is {{ item.name }} and Age is {{ item.age }}</li>
</ul>

</template>

<script>
export default{
    name: 'IfElse',
    data(){
        return{
            msg: 0,
            technology: ['Java', 'PHP', 'Python', 'Ruby'],
            profiles: [
                {
                    name: "Raju Dey",
                    age: "24"

                },
                {
                    name: "Jack",
                    age: "25"
                },
                {
                    name: "Miller",
                    age: "26"
                }
            ]
        }
    }
}
</script>