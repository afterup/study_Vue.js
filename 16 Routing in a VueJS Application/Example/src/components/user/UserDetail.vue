<template>
    <div>
        <h3>Some User Details</h3>
        <p>ID: {{ $route.params.id }}</p>
        <router-link tag="button" 
                     :to="link"
                     class="btn btn-warning"> Edit </router-link>
                
    </div>
</template>

<script>
    export default {
        data(){
            return {
                link: { 
                    name:'userEdit',
                    params:{ id:this.$route.params.id }, 
                    query:{ locale:'en', key:'one'},
                    hash: "#data"
                }
            }
        },
        beforeRouteEnter(to, from, next){
            if(true){
                next();
            }else{
                next(false);
            }
        }
    }
</script>