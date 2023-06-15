<template>
    <section id="Works" class="container pt-3 ms_margin">
        <h2 class="d-inline-block px-3 rounded-2 mb-5 mt-5">Progetti</h2>
        <div class="row justify-content-between ms_center">
            <div v-for="(card, index) in cards" :key="index" class="col-7 col-sm-5 col-lg-3 ms_p-0 mb-5 mx-3">
                <div @click="nextIndex(index), trueFalse()"  class="card w-100" style="cursor: pointer;">
                    <img class="card-img-top" :src="card.img" alt="Card image cap">
                    <div class="card-body">
                        <h3 class="card-text">{{ card.title }}</h3>
                    </div>
                </div>
            </div>
        </div>    
        <div class="ms_f" v-if="isTrue">
            <div class="text-end p-1">
                <span class="d-inline-block">
                    <i class="p-2 ms-4 rounded-5 fa-solid fa-x fs-3 mx-3 ms_x ms_xe ms_icon" :class="cards[activeIndex].class" @click="xWork()"></i>
                </span>
            </div>   
            <div class="row justify-content-center">
                <div class="col-lg-7 col-md-8  col-10"><img class="rounded-5" :src="cards[activeIndex].img" alt=""></div> 
                <div class="col-lg-4 col-md-4  col-10 pt-3 position-relative">
                    <div class="ms_text  rounded-3 p-4" :class="cards[activeIndex].class">
                        <h3 class="mb-3">{{ cards[activeIndex].title }}</h3>
                        <p class="fs-5 mb-3">{{ cards[activeIndex].description }}</p>
                        <div class="fs-5 mb-3">{{ cards[activeIndex].tecnologie }}</div>
                    </div>
                </div>
            </div> 
            <div class="position-fixed ms_bottom mb-2">
                <span class="d-inline-block col-5">
                    <i class="p-2 ms-4 rounded-5 fa-solid fa-arrow-left fs-3 ms_icon ms_x" :class="cards[activeIndex].class" @click="beforeWork()"></i>
                </span>
                <span class="d-inline-block ms_w text-end">
                    <i class="fa-solid fa-arrow-right fs-3 p-2 rounded-5 ms_icon ms_x" :class="cards[activeIndex].class" @click="nextWork()"></i>
                </span>
            </div>   
        </div>
    </section>
</template>

<script>

export default {
  components: { },

  data(){
        return{
            isTrue: false,
            activeIndex: 0,
            cards: [
                {
                    img: require('@/assets/comics-img.png'),
                    title: 'Comics',
                    description: 'Una pagina che riproduce il sito web originale dei fumetti DC creato utilizzando VueJs. Ogni sezione è composta da diversi componenti e popolata da array di oggetti',
                    tecnologie: 'Tecnologie: Html, SCSS, Bootstrap, JavaScript, Vue.',
                    class: 'ms_blue',
                },
                {
                    img: require('@/assets/discord-img.png'),
                    title: 'Discord',
                    description: 'Una pagina Web di base che riproduce la Home page di Discord utilizando le prime prorpieta di css. Riproducendo prima uno scheletro della pagina e in seguito aggiunti i contenuti',
                    tecnologie: 'Tecnologie: Html, CSS.',
                    class: 'ms_blue',
                },
                {
                    img: require('@/assets/Immagine 2022-10-06 182244.png'),
                    title: 'Dropbox',
                    description: 'Un altro progetto front-end realizzato con Html e CSS. Dropbox il servizio più diffuso di file hosting.',
                    tecnologie: 'Tecnologie: Html, CSS.',
                    class: 'ms_light_grey',
                },
                {
                    img: require('@/assets/deliveboo.png'),
                    title: 'Deliveboo',
                    description: 'Progetto sviluppato in team, una pagina web che prende spunto da deliveroo. Progetto curato sia nella parte back-end che front-end permettendo al ristoratore di gestire piatti e ordini, e al cliente di effetuare ordini e ricerche incrociate.',
                    tecnologie: 'Tecnologie: MySql, PHP, Laravel, Htm, CSS, JavaScript, Vue',
                    class: 'ms_red',
                },/* 
                {
                    img: require('@/assets/sony-img.png'),
                    title: 'Sony',
                    description: 'Introduzione al Front-end: una pagina Web di base che riproduce la Home page di Playstation utilizzando Bootstrap. Reattivo al 100% per il telefono cellulare.',
                    tecnologie: '',
                },
                {
                    img: require('@/assets/spotify-img.png'),
                    title: 'Spotify',
                    description: 'Un altro progetto front-end realizzato con Bootstrap. Ho riprodotto la Home page di Spotify Web App. Completamente reattivo.',
                    tecnologie: '',
                }, */
            ]
        }
    },

    methods:{
        nextIndex(index){
            this.activeIndex = index;   
            console.log(this.activeIndex);
        },

        trueFalse(){
            this.isTrue = true;
            console.log(this.isTrue);
        },

        nextWork(){
            this.activeIndex ++
            if(this.activeIndex === this.cards.length){
                this.activeIndex = 0
            }
        },

        beforeWork(){
            this.activeIndex --
            if(this.activeIndex < 0){
                this.activeIndex = this.cards.length - 1
            }
        },

        xWork(){
            this.isTrue = false;
        }
    }
}
</script>

<style lang="scss" scoped>

.ms_margin{
    margin-top: 170px;


    h2{
        background-color: green;
        color: white;
    }

}


.ms_p-0{
    padding: 0;
}

.ms_img{
    object-fit: fill;
    object-position: top;
}

.ms_f{
    background-color: rgba(7, 7, 7, 0.34);
    width: 100vw;
    height: 100vh;
    position: fixed;
    z-index: 2;
    top: 0;
    left: 0;
    overflow: hidden;

    img{
        width: 100%;
        
    }


    .ms_text{
        color: white;
    }

    .ms_w{
        width: 55%;
    }

    .ms_blue{
        border: 2px solid #006EFF;
        background-color: #006EFF;
        color: white;
    }

    .ms_light_grey{
        border: 2px solid lightgray;
        background-color: lightgrey;
        color: black;
    }

    .ms_red{
        border: 2px solid red;
        background-color: red;
        color: white;
    }

    .ms_icon:hover{
        border: 2px solid white;
    }

    .ms_x{
        cursor: pointer;
    }

    .ms_bottom{
        bottom: 0;
        width: 100%;
    }
}


@media screen and (max-width: 600px) {
    .ms_center{
        justify-content: center !important;
    }
}


@media screen and (min-width: 768px) {

    .ms_text{
        position: absolute;
        top: 150px;
        left: -50px;
    }

}

@media screen and (min-width: 1200px) {

    .ms_text{
        position: absolute;
        top: 200px;
        left: -50px;
    }
} 
</style>