<template>
    <h5>Student Name is: {{ name }}</h5>
</template>

<script>
export default{
    name: 'StudentsDetails',
    props: {
    name: String
    }
}
</script>