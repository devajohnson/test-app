<template>

    <form @submit.prevent="create">
        <input v-module="form.title" id="title" placeholder="Title">
        <input v-model="form.userId"  id="userId" placeholder="User Id">
        <!-- <input v-model="form.body" id="body" placeholder="Body"> -->
        <textarea v-model="form.body" id="body" placeholder="Body"></textarea>
        <button>create</button>
    </form>
</template>

<script>
import axios from 'axios' 
export default {
    name:'Postelement',
    data(){
        return{
            form:{
            title:'',
            userId:'',
            body:''
            },
            data:[],
            obj:''

            
        }
    },
    methods:{
        create(){
            axios.post(' https://curp-renapo.p.rapidapi.com/v1/curp/posts',this.form)
            .then((repo)=>{
                console.log(repo.data);
            })
        }
    }
}
</script>
