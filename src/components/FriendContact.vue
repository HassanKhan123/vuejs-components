<template>
    <li>
    <h2>{{name}}</h2>
    <button @click="toggleDetails">{{detailsAreVisible?'Hide':'Show'}} Details</button> 
    <ul v-if="detailsAreVisible">
        <li><strong>Email: </strong>{{email}}</li>
        <li><strong>Phone: </strong>{{phoneNumber}}</li>

    </ul>
    </li>
</template>

<script>
export default {
    props:['name','email','phoneNumber'],
    data(){
        return{
            detailsAreVisible:false,
          
        }
    },
    methods:{
        toggleDetails(){
            this.detailsAreVisible=!this.detailsAreVisible
        }
    }
}
</script>