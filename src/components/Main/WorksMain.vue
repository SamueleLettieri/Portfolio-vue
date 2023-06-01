<template>
    <section id="Works" class="container pt-5 ms_margin">
        <h2 class="d-inline-block px-3 rounded-2 mb-5 mt-5">Progetti</h2>
        <div class="row justify-content-between">
            <div  v-for="(card, index) in cards" :key="index"  @click="nextIndex(index), trueFalse()" class="card col-4 mx-5 ms_p-0 mb-5" style="width: 18rem; cursor: pointer;">
                <img class="ms_img card-img-top" :src="card.img" alt="Card image cap">
                <div class="card-body">
                    <h3 class="card-text">{{ card.title }}</h3>
                </div>
            </div>
        </div>    
        <div class="ms_f" v-if="isTrue">
            <div class="text-end p-5">
                <span class="d-inline-block mt-2">
                    <i class="p-2 ms-4 rounded-5 fa-solid fa-x fs-3 ms_x ms_xe" @click="xWork()"></i>
                </span>
            </div>   
            <div>
                <div class="ms_img d-inline-block"><img class="rounded-5" :src="cards[activeIndex].img" alt=""></div> 
                <div class="ms_text d-inline-block rounded-3 p-4">
                    <h3 class="mb-3">{{ cards[activeIndex].title }}</h3>
                    <p class="fs-5 mb-3">{{ cards[activeIndex].description }}</p>
                    <div class="fs-5 mb-3">{{ cards[activeIndex].tecnologie }}</div>
                </div>
            </div> 
            <div class="">
                <span class="d-inline-block col-5">
                    <i class="p-2 ms-4 rounded-5 fa-solid fa-arrow-left fs-3 ms_arrow ms_x" @click="beforeWork()"></i>
                </span>
                <span class="d-inline-block ms_w text-end">
                    <i class="fa-solid fa-arrow-right fs-3 ms_arrow p-2  rounded-5 ms_x" @click="nextWork()"></i>
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
                },
                {
                    img: require('@/assets/discord-img.png'),
                    title: 'Discord',
                    description: 'Una pagina Web di base che riproduce la Home page di Discord utilizando le prime prorpieta di css. Riproducendo prima uno scheletro della pagina e in seguito aggiunti i contenuti',
                    tecnologie: 'Tecnologie: Html, CSS.',
                },
                {
                    img: require('@/assets/Immagine 2022-10-06 182244.png'),
                    title: 'Dropbox',
                    description: 'Un altro progetto front-end realizzato con Html e CSS. Dropbox il servizio più diffuso di file hosting.',
                    tecnologie: 'Tecnologie: Html, CSS.',
                },
                {
                    img: require('@/assets/deliveboo.png'),
                    title: 'Deliveboo',
                    description: 'Progetto sviluppato in team, una pagina web che prende spunto da deliveroo. Progetto curato sia nella parte back-end che front-end permettendo al ristoratore di gestire piatti e ordini, e al cliente di effetuare ordini e ricerche incrociate.',
                    tecnologie: 'Tecnologie: MySql, PHP, Laravel, Htm, CSS, JavaScript, Vue',
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

    img{
        width: 100%;
        
    }

    .ms_img{
        width: 60%;
        position: relative;
        top: 0px;
        left: 100px;
    }

    .ms_text{
        background-color: lightgray;
        position: relative;
        top: 400px;
        right: 50px;
        width: 30%;
    }

    .ms_w{
        width: 55%;
    }

    .ms_arrow:hover{
        border: 2px solid black;
    }

    .ms_x{
        cursor: pointer;
    }
}

</style>