<template>
  <div class="d-flex justify-content-between align-items-center w-50">
    <div class="d-flex flex-column w-100">
      <label class="from-label my-2">شهرستان:</label>
      <select
        class="form-select"
        v-model="form.city"
        aria-label="Default select example"
      >
        <option selected disabled>شهرستان</option>
        <option v-for="(city, key) in cities" :key="key" :value="city">
          {{ city }}
        </option>
      </select>
    </div>
    <span style="padding: 0px 25px" />
    <div class="d-flex flex-column w-100">
      <label class="from-label my-2">استان:</label>
      <select
        class="form-select"
        v-model="form.province"
        aria-label="Default select example"
      >
        <option selected disabled>استان</option>
        <option
          v-for="(province, key) in provinces"
          :key="key"
          :value="province.id"
        >
          {{ province.name }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
import provinces from "../Data/provinces";
import cities from "../Data/cities";

export default {
  data() {
    return {
      form: {
        city: "",
        province: "",
      },
    };
  },
  computed: {
    provinces() {
      return provinces;
    },
    cities() {
      let city = [];
      console.log(cities);
      for (let i = 0; i < cities.length; i++) {
        if (cities[i].province_id == this.form.province) {
          city.push(cities[i].name);
        }
      }
      return city;
    },
  },
};
</script>

<style scoped>
div {
  text-align: right;
}
</style>
