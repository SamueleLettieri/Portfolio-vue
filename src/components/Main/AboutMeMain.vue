<template>
  <section id="About-Me" class="container pt-5 ms_margin">
    <div>
        <div class="row">
        <div class="col-lg-6 col-12">
            <h2 class="d-inline-block px-3 rounded-2">Chi Sono</h2>
            <div class="ps-3">
                <p class="fs-5">Siccome vivevo in una località turistica, sono entrato nel mondo del lavoro durante il periodo delle superiori, cominciando da una piccola pasticceria e cambiando di stagione in stagione un locale, non era una vera e propria aspirazione.</p>
                <p class="fs-5">Al mio quinto anno di alberghiero la mia scuola mise in palio una borsa di studio per i migliori 4 studenti dell'istituto, e decisi di sfruttare questa opportunità per realizzare la mia grande passione di lavorare nell'informatica, mi impegnai tanto per vincere la borsa di studio e alla fine ci riuscì.</p>
                <p class="fs-5">Sono sempre stato interessato alla tecnologia e all'informatica.</p>
                <p class="fs-5">Decisi di iscrivermi all'università Federico II di Napoli al corso di ingegneria informatica, e consolidare le basi pratiche frequentando un corso intensivo per diventare Full Stack Web Developer!</p>
            </div>
        </div>
        <div class="col-lg-6 text-center col-12"><img src="../../assets/samImg.jpg" alt=""></div>
        </div>
    </div>    
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

.ms_margin{
    margin-top: 170px;

    h2{
        background-color: green;
        color: white;
    }

    img{
        width: 400px;
    }
}

@media screen and (max-width: 475px) {
    img{
        width: 300px !important;
    }
}
</style>