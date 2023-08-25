<template>
    <h5>Teacher Name is: {{ name }}</h5>
</template>

<script>
export default{
    name: 'TeacherDetails',
    props: {
        name: String
    }
}
</script>