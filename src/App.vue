<template>
  <section>
    <h2>My Friends</h2>
    <ul>
        <friend-contact></friend-contact>
        <friend-contact></friend-contact>
    </ul>
  </section>
</template>

<script>
export default {
    data(){
        return{
            friends:[
                {
                    id:'1',
                    name:'Hassan',
                    email:'hassan@gmail.com',
                    phone:'03243219156'
                },
                {
                    id:'2',
                    name:'Khan',
                    email:'khan@gmail.com',
                    phone:'03243219156'
                }
            ]
        }
    }
};
</script>