<template>
    <div class="ml-3">
        <!-- <p>{{msg}}</p> -->
        <table class="gettable">
            <thead>
                <tr>
                    <th scope="col">SI</th>
                    <th scope="col">Title</th>
                    <th scope="col">user Id</th>
                    <th scope="col">body</th>

                </tr>
            </thead>
            <tbody v-for="key in data" :key="key.id">
                <tr>
                <td>{{key.id}}</td>
                <td>{{key.title}}</td>
                <td>{{key.userId}}</td>
                <td>{{key.body}}</td>
                </tr>
            </tbody>
        </table>
    </div>
    
</template>
<script>

import axios from 'axios'

export default {
    name: 'Getelement',
 
    data(){
        return{
            data:[]
        }
    },
    created(){
        this.apicall()
    },
    methods:{
        apicall(){
            // axios.get('https://jsonplaceholder.typicode.com/posts')
            axios.get('https://mocki.io/v1/cb410377-80d8-407f-a246-0d3f81829cd4')
            .then((responce)=>
            this.data = responce.data)
            console.log(this.data)
        }
    }
}
</script>
