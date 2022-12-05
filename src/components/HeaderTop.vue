<template>

    <div>
         <h1>  {{siteTitle}} </h1>
    </div>
</template>

<script>

    export default{
        name : 'HeaderTop',
        props: {
            siteTitle: String
        }
    }
</script>

<style scoped>

div{
    text-align: center;
}
</style>