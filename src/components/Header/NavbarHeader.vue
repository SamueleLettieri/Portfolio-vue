<template>
<nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
        <a class="navbar-brand" href="#Welcome"><img src="../../assets/logo.jpg" alt=""></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item" v-for="(anchor, index) in anchors" :key="index">
                    <a class="nav-link active" aria-current="page" :href="anchor.link">{{anchor.voice}}</a>
                </li>
            </ul>
        </div>
    </div>    
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
    background-color: rgb(34, 177, 76) !important;
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 1;


        a{
            text-decoration: none;
            color: black;
        }

        a:hover{
            color: white;
        }
    

    li:hover{
        background-color: rgba(255,255,255,0.34);
    }

    img{
        height: 55px;
    }
}

</style>