<template>
  <nav class="d-flex col-12">
    <ul class="col-6 ">
        <li class="d-inline-block" v-for="(anchor, index) in anchors" :key="index">
            <a class="d-inline-block p-3 pe-4" :href="anchor.link">{{anchor.voice}}</a>
        </li>
    </ul>
    <div class="text-end col-6 pe-3"><img class="" src="../../assets/logo.png" alt=""></div>
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
                    link: '#',
                },
                {
                    voice: 'Progetti',
                    link: '#',
                },
                {
                    voice: 'Contatto',
                    link: '#',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
nav{
    background-color: rgb(34, 177, 76);
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