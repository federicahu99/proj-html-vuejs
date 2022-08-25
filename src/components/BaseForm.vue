<template>
  <div>
    <form class="row g-3" @keyup.enter="registerRequest">
      <div class="col-md-6">
        <label for="inputEmail4" class="form-label m-2">Email</label>
        <input
          type="email"
          class="form-control"
          id="inputEmail4"
          placeholder="samking1994@gmail.com"
          v-model="email"
        />
      </div>
      <div class="col-md-6">
        <label for="inputAddress" class="form-label m-2"
          >Name and Lastname</label
        >
        <input
          type="text"
          class="form-control"
          id="inputAddress"
          placeholder="Sam King"
          v-model="nameSurname"
        />
      </div>
      <div class="col-md-6">
        <label for="inputAddress" class="form-label m-2">Phone number</label>
        <input
          type="text"
          class="form-control"
          id="inputAddress"
          placeholder="917-813-8861"
          v-model="phone"
        />
      </div>
      <div class="col-md-6">
        <label for="inputCity" class="form-label m-2">City</label>
        <input
          type="text"
          class="form-control"
          id="inputCity"
          placeholder="New York"
          v-model="city"
        />
      </div>
      <div class="col-12" id="states">
        <label for="inputState" class="form-label m-2">State </label>
        <select id="inputState" class="form-select" v-model="state">
          <option selected>Choose...</option>
          <option v-for="(country, i) in countries" :key="i">
            {{ country }}
          </option>
        </select>
      </div>
      <div class="col-12">
        <button id="button-quote" class="m-3" @click="registerRequest">
          Request an Appoitment
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "BaseForm",
  props: {
    countries: Array,
  },
  data() {
    return {
      email: "",
      nameSurname: "",
      phone: "",
      city: "",
      state: "",
    };
  },
  methods: {
    registerRequest() {
      console.log(
        `Email: ${this.email}, NameSurname: ${this.nameSurname}, Phone: ${this.phone}, City: ${this.city}, State: ${this.state} `
      );
      if (
        !this.email ||
        !this.nameSurname ||
        !this.phone ||
        !this.city ||
        !this.state
      ) {
        alert("All the fields MUST be compiled");
      } else {
        alert("Request send successfully! We will Contact you within 3 working days!");
          (this.email = ""),
          (this.nameSurname = ""),
          (this.phone = ""),
          (this.city = ""),
          (this.state = "");
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_var.scss";

#states {
  margin: 20px 0;
}

button {
  font-size: 13px;
  text-transform: capitalize;
  padding: 8px 12px;
  border-radius: 22px;
  border-color: $denim;
  background-color: $denim;
  color: white;
  border: 0px;
  transition: 0.4s;

  &:hover,
  &:active {
    outline: 0;
    border: 2px solid $mercury; // rivedere !!!!!!!!!!!
    color: $mercury;
    font-weight: bold;
    background-color: dodgerblue;
    border: none;
    scale: 104%;
  }
}
</style>