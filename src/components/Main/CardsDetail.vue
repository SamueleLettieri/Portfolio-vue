<template>
    <div class="ms_f">
<!--         <div>
            <div class="ms_img d-inline-block"><img class="rounded-5" :src="cards[activeIndex].img" alt=""></div> 
            <div class="ms_text d-inline-block rounded-3 p-4">
                <h3 class="mb-3">{{ cards[activeIndex].title }}</h3>
                <p class="fs-5 mb-3">{{ cards[activeIndex].description }}</p>
                <div class="fs-5 mb-3">{{ cards[activeIndex].tecnologie }}</div>
            </div>
        </div> 
        <div class="">
            <span class="d-inline-block col-5">
                <i class="p-2 ms-4 rounded-5 fa-solid fa-arrow-left fs-3 ms_arrow"></i>
            </span>
            <span class="d-inline-block ms_w text-end">
                <i class="fa-solid fa-arrow-right fs-3 ms_arrow p-2  rounded-5" ></i>
            </span>
        </div>   --> 
    </div>
</template>

<script>
export default {
    props: {
        cards: {
            type: Array,
            required: true
        },
        activeIndex: {
            type: Number,
            required: true
        }
    },

    data(){
        return{
            localIndex: this.activeIndex,
        }
    },

    methods:{
        nextIndex(){
            this.localIndex++;   
        },

    }
}
</script>

<style lang="scss" scoped>
.ms_f{
    background-color: rgba(7, 7, 7, 0.34);
    width: 100vw;
    height: 100vh;
    position: fixed;
    z-index: 2;
    top: 0;
    left: 0;

    img{
        width: 100%;
        
    }

    .ms_img{
        width: 60%;
        position: relative;
        top: 100px;
        left: 100px;
    }

    .ms_text{
        background-color: lightgray;
        position: relative;
        top: 500px;
        right: 50px;
        width: 30%;
    }

    .ms_w{
        width: 55%;
    }

    .ms_arrow:hover{
        border: 2px solid black;
    }
}

</style>