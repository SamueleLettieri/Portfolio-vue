<template>
  <nav class="d-flex col-12">
    <ul class="col-6 ">
        <li class="d-inline-block p-3" v-for="(anchor, index) in anchors" :key="index">
            <a :href="anchor.link">{{anchor.voice}}</a>
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
                    link: '#',
                },
                {
                    voice: 'Competenze',
                    link: '#',
                },
                {
                    voice: 'Competenze',
                    link: '#',
                },
                {
                    voice: 'Progetti',
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
        border-bottom: 1px solid white;
    }

    img{
        height: 55px;
    }
}

</style>