<template>
  <h3>{{movieTitle}}</h3>
</template>

<script>
export default {
    // props: ['movieTitle']
    props: {
        movieTitle: {
            type: String,
            //required: true,
            default() {
                return 'no title';
            }
        }
    }
}
</script>

<style>

</style>