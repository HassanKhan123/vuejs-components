<template>
  <form @submit.prevent="submitHandler">
    <div>
      <label>Name</label>
      <input type="text" v-model="name" />
    </div>
    <div>
      <label>Phone</label>
      <input type="tel" v-model="phone" />
    </div>
    <div>
      <label>Email</label>
      <input type="email" v-model="email" />
    </div>
    <div>
      <button>Add Contact</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      phone: "",
    };
  },
  emits: ["add-contact"],
  methods: {
    submitHandler() {
      this.$emit("add-contact", this.name, this.email, this.phone);
    },
  },
};
</script>