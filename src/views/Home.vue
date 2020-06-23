<template>
  <div class="home">
    <formInfo />
  </div>
</template>

<script>
// @ is an alias to /src
import formInfo from "@/components/formInfo.vue";

export default {
  name: "Home",
  components: {
    formInfo
  }
};
</script>
