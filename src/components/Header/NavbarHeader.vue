<template>
<nav class="d-flex flex-wrap">
    <ul class="col-lg-6 col-md-12">
        <li class="d-inline-block" v-for="(anchor, index) in anchors" :key="index">
            <a class="d-inline-block p-3 pe-lg-4" :href="anchor.link">{{anchor.voice}}</a>
        </li>
    </ul>
    <div class="text-end col-lg-6 col-md-12 pe-3"><a class="me-3" href="#Welcome"><img class="" src="../../assets/logo.jpg" alt=""></a></div>
</nav>
</template>

<script>
export default {
    data() {
        return {
            anchors:[ 
                {
                    voice: 'Chi Sono',
                    link: '#About-Me',
                },
                {
                    voice: 'Competenze',
                    link: '#Skills',
                },
                {
                    voice: 'Progetti',
                    link: '#Works',
                },
                /* {
                    voice: 'Contatto',
                    link: '#',
                }, */
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
nav{
    background-color: rgb(34, 177, 76);
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 1;
    ul{
        padding: 0;
        margin: 0;
    }
    li{
        list-style: none;

        a{
            text-decoration: none;
            color: black;
        }

        a:hover{
            color: white;
        }
    }

    li:hover{
        background-color: rgba(255,255,255,0.34);
    }

    img{
        height: 55px;
    }
}

</style>