<template>
    <footer> 
        <div class="row text-center align-items-center w-100 ms_white">
            <div class="col-6">
                <ul class="navbar-nav d-inline-block">
                    <li class="nav-item d-inline-block me-2" v-for="(contact, index) in contacts" :key="index">
                        <a class="nav-link active " aria-current="page" :href="contact.link"><i class="fs-2" :class="contact.icon"></i></a>
                    </li>
                </ul>   
            </div>
            <div class="col-6 fs-5">
                Email: samuele2073atmail.com
            </div>
        </div>    
    </footer>
</template>
    
<script>
    export default {
        data() {
            return {
                contacts:[ 
                    {
                        icon: 'fa-brands fa-github',
                        link: 'https://github.com/SamueleLettieri',
                    },
                    {
                        icon: 'fa-brands fa-linkedin',
                        link: 'https://www.linkedin.com/in/samuele-lettieri-a24681251/',
                    },
                ]
            }
        }
    }
</script>
    
<style lang="scss" scoped>
footer{
    background-color: rgb(34, 177, 76) !important;


        a{
            text-decoration: none;
        }

        .ms_white{
            color: white;
        }

}
    
</style>