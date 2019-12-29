<template>
  <div class="home">
    <h1>This is home page</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import { fetchData } from '@/api/index';

export default {
  name: 'home',
  mounted() {
    fetchData()
      .then((data) => {
        console.log(data);
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>
