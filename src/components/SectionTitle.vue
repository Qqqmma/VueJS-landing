<template>
<div class="section-title">
    <div class="container-1170">
        <h2 :class="color + ' title'">{{ title }}</h2>
        <p :class="color + ' description'">{{ description }}</p>
    </div>
</div>
</template>


<script>
export default {
    props: ['title', 'description', 'color'],
}
</script>


<style scoped>
.black{
    color: #394b50;
}
.white{
    color: #fff;
}
.title{
    font-family: 'Open Sans', sans-serif;
    font-weight: 700;
    font-size: 28px;
    text-transform: uppercase;
    text-align: center;
}
.description{
    font-family: 'Open Sans', sans-serif;
    font-weight: 400;
    font-size: 14px;
    text-align: center;
}
</style>