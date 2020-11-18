<template>
  <li>
    <h2>{{ name }} {{ isFavourite === "1" ? "- (Favourite)" : "" }}</h2>
    <button @click="toggleDetails">
      {{ detailsAreVisible ? "Hide" : "Show" }} Details
    </button>
    <ul v-if="detailsAreVisible">
      <li><strong>Email: </strong>{{ email }}</li>
      <li><strong>Phone: </strong>{{ phoneNumber }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  // props:['name','email','phoneNumber'],
  props: {
    name: {
      type: String,
      required: true,
    },
    email: {
      type: String,
      required: true,
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    isFavourite: {
      type: String,
      required: false,
      default: "0",
      validator: (value) => {
        return value === "1" || value === "0";
      },
    },
  },
  data() {
    return {
      detailsAreVisible: false,
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>