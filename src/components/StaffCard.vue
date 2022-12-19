<template>  
    <div class="col col-6 col-lg-4 px-3 px-md-5">
        <img :src="require('@/'+imgSrc)"/>
        <div id="name">{{ Name }}</div>
        <div id="post">{{ post }}</div>
    </div>
</template>

<script>
export default {
    props:{
        imgSrc: String,
        Name: String,
        post: String
    }
};
</script>

<style scoped>
div.col {
    padding: 0 50px;
    margin-bottom: 70px;
    max-width: 380px;
}
img{
    width: 100%;
    margin-bottom: 25px;
}
#name{
    font-weight: bold;
    font-weight: bold;
    line-height: 1.37;
    color: #050c33;
    text-decoration: none;
    display: inline-block;
    margin-bottom: 5px;
}
#post{
    padding: 0;
    color: #505570;
    font-weight: 500;
    font-size: 16px;
    line-height: 1.37;
    margin-bottom: 5px;
}
</style>
