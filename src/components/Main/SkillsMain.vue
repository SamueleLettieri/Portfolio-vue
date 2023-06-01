<template>
  <section id="Skills" class="ms_margin fs-5 pt-5">
    <div class="container mt-5">
        <h2 class="d-inline-block px-3 rounded-2 mb-5 mt-5">Competenze</h2>
        <div class="row justify-content-center">
            <div>
                <ul class="text-center mb-5">
                    <li class="cursor ms_m rounded-2 d-inline-block px-3 pt-1 pb-1 ms_bored" v-for="(skill, i) in skills" :key="i" :class="{'ms_active': activeIndex === i}" @click="nextindex(i)">{{skill.title}}</li>
                </ul>
            </div>
            <div class="row ms_h">
                <div class="col-5">
                    <ul class="row  text-center">
                        <li class=" mt-5 pt-2" :class="{'text-end': index === 0 || index === 1}" v-for="(miniTitle, index) in skills[activeIndex].miniTitles" :key="index"><span class="cursor ms_b d-inline-block px-3 pt-1 pb-1 mx-5  rounded-2" :class="{'ms_bor': newIndex === index}" @click="newI(index)">{{ miniTitle.titolino }}</span></li>
                    </ul>
                </div>
                <div class="col-7">
                    <ul>
                        <li class="w-50 mt-1" v-for="(competenza, index) in skills[activeIndex].miniTitles[newIndex].competenze" :key="index"><span class="mx-3"><i :class="competenza.icona"></i></span> {{ competenza.tecnologie }} <hr></li>
                    </ul>
                </div>
            </div>    
        </div>
    </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            isTrue: true,
            activeIndex: 0,
            newIndex: 0,
            skills: [
                {
                    title: "Hard Skills",
                    miniTitles: [
                        {
                            titolino: "Frontend",
                            competenze: [
                                {
                                    icona:"fa-brands fa-html5",
                                    tecnologie: "HTML"
                                },
                                {
                                    icona:"fa-brands fa-css3",
                                    tecnologie: "CSS"
                                },
                                {
                                    icona:"fa-brands fa-sass",
                                    tecnologie: "Sass"
                                },
                                {
                                    icona:"fa-brands fa-bootstrap",
                                    tecnologie: "Bootstrap"
                                },
                                {
                                    icona:"fa-brands fa-square-js",
                                    tecnologie: "JavaScript"
                                },
                                {
                                    icona:"fa-brands fa-vuejs",
                                    tecnologie: "Vue.js"
                                },
                            ]
                        },
                        {
                            titolino: "Backend",
                            competenze: [
                                {
                                    icona:"fa-solid fa-compact-disc",
                                    tecnologie: "Mysql"
                                },
                                {
                                    icona:"fa-brands fa-php",
                                    tecnologie: "PHP"
                                },
                                {
                                    icona:"fa-brands fa-laravel",
                                    tecnologie: "Laravel"
                                },
                                {
                                    icona:"fa-brands fa-java",
                                    tecnologie: "Java"
                                },
                                {
                                    icona:"fa-brands fa-spring",
                                    tecnologie: "Spring"
                                },
                            ]
                        },
                    ]
                },
                {
                    title: "Soft Skills",
                    miniTitles: [
                        {
                            titolino: "Personali",
                            competenze: [
                                {
                                    icona:"fa-solid fa-bullseye",
                                    tecnologie: "Motivazione"
                                },
                                {
                                    icona:"fa-solid fa-arrow-up-right-dots",
                                    tecnologie: "Volontà di migliorare"
                                },
                                {
                                    icona:"fa-solid fa-stopwatch",
                                    tecnologie: "Gestione del tempo"
                                },
                            ]
                        },
                        {
                            titolino: "Sociali",
                            competenze: [
                                {
                                    icona:"fa-solid fa-handshake",
                                    tecnologie: "Lavoro si squadra"
                                },
                                {
                                    icona:"fa-solid fa-bullhorn",
                                    tecnologie: "comunicazione"
                                },
                                {
                                    icona:"fa-solid fa-hand-holding-heart",
                                    tecnologie: "Empatia"
                                },
                                {
                                    icona:"fa-solid fa-stopwatch",
                                    tecnologie: "Capacita d'adatamento"
                                },
                            ]
                        },
                    ]
                },
            ],
        }
    },

    methods:{
        nextindex(index){
            this.activeIndex  = index;   
        },

        newI(index){
            this.newIndex  = index;
            console.log(this.newIndex)
        }
    }

}
</script>

<style lang="scss" scoped>

.ms_margin{
    margin-top: 170px;

    .ms_t-e{
        align-items: end;
    }

    li {
        list-style: none;
    }

    h2{
        background-color: green;
        color: white;
    }

    .cursor:hover{
        cursor: pointer;
    }

    .ms_bored{
        border: 1px solid green;
        color: green;
    }

    .ms_bored:hover{
        background-color: green;
        color: white;
    }

    .ms_active{
        background-color: green;
        color: white;
    }

    .ms_bor{
        border-bottom: 3px solid green;
    }

    .ms_b:hover{
        border-bottom: 3px solid green;
    }

    hr{
        border: 1px solid green;
    }

    .ms_h{
        height: 375px;
    }
    .ms_m{
        margin-right: 150px;
    }
}
</style>