
<!-- 
    1 - карточка с 'фоном наполовину'
    2 - большая карточка
    3 - карточка с 'полным фоном'
 -->
<template>
    <div v-if="tp===1" class="col col-12 col-sm-6 col-md-4">
        <div id="card">
            <img id="pic1" :src="require('@/'+image)"/>
            <div class="text text1">
                <h2 id="name">{{ title }}</h2>
                <div id="date">{{ date }}</div>
                <div id="content">{{ content }}</div>
            </div>
        </div>
    </div>
    <div v-else-if="tp===2" class="col col-12 col-sm-6 col-md-8">
        <div id="card">
            <img :src="require('@/'+image)"/>
            <div class="text text2">
                <h2 id="name">{{ title }}</h2>
            </div>
        </div>
    </div>
    <div v-else class="col col-12 col-sm-6 col-md-4">
        <div id="card">
            <img :src="require('@/'+image)"/>
            <div class="text text3">
                <h2 id="name">{{ title }}</h2>
                <div id="date3">{{ date }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        cs: {}
    },
    data(){
        return{
            tp : this.cs.type,
            image : this.cs.image,
            date : this.cs.date,
            title : this.cs.title,
            content : this.cs.content
        }
    }
};
</script>

<style scoped>
#card{
    margin: 0 10px;
    float: left;
    margin-bottom: 20px;
    font-family: Montserrat;
    overflow: hidden;
    cursor: pointer;
    border-radius: 5px;
    position: relative;
    height: 475px;
    width: -webkit-fill-available;
}
#card::before{
    content: "";
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 5;
    border-radius: 5px;
}
img{
    width: 100%;
    height: 100%;
    height: 475px;
    object-fit: cover;
    max-width: 100%;
}
img#pic1{
    height: 215px;
}
#name{
    font-weight: bold;
    line-height: 1.37;
    color: white;
    text-decoration: none;
    display: inline-block;
    margin-bottom: 5px;
    font-size: 18px;

}
#content{
    padding: 0;
    color: #505570;
    font-weight: 500;
    font-size: 14px;
    line-height: 1.37;
    margin-bottom: 5px;
}
#date{
    color: #050c33;
    font-size: 12px;
}
#date3{
    color: white;
    font-size: 12px;
}
.text{
    position: static;
    padding: 40px 30px 30px;
}
.text2{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 10;
    padding: 35px 40px;
}
.text3{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 10;
    padding: 50px 40px;
}

.text1>#name{
    color: #050c33;
}
@media (max-width: 600px){
    img#pic1{
        height: auto;
    }
}

@media (max-width: 767px){
    img{
        height: 360px;
    }
    img#pic1{
        height: 200px;
    }
    #card{
        height: auto;
    }
}
@media (max-width: 1080px){
    #name{
        font-size: 14px;
    }
    #content{
        font-size: 12px;
    }
    .text{
        padding: 20px 15px 15px;
    }
    
}
</style>
