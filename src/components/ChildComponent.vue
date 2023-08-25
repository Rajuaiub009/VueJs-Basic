<template>

        <h2>{{ data.name }}</h2>
        <h2>{{ data.age }}</h2>
        <button @click="getData(data.name)">Show Details</button>
    
</template>

<script>
export default{
    name: 'ChildComponent',
    props: {
        data: Object,
        getData: Function
    }
}
</script>