<template>
    <h2>Hai i selman, {{ name }}</h2>
</template>


<script>
export default {
    name: "SElman",
    props: ['name']
};
</script>


<style>
h2{
  text-align: center;
}
</style>