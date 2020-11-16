<template>
    <li>
    <h2>{{friend.name}}</h2>
    <button @click="toggleDetails">{{detailsAreVisible?'Hide':'Show'}} Details</button> 
    <ul v-if="detailsAreVisible">
        <li><strong>Email: </strong>{{friend.email}}</li>
        <li><strong>Phone: </strong>{{friend.phone}}</li>

    </ul>
    </li>
</template>

<script>
export default {
    data(){
        return{
            detailsAreVisible:false,
            friend:{
                    id:'1',
                    name:'Hassan',
                    email:'hassan@gmail.com',
                    phone:'03243219156'
                },
        }
    },
    methods:{
        toggleDetails(){
            this.detailsAreVisible=!this.detailsAreVisible
        }
    }
}
</script>