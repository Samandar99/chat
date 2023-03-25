<template>
  <div class="container">
    <UserOne />
    <UserTwo />
  </div>
</template>

<script>
import UserOne from "@/components/UserOne.vue";
import UserTwo from "@/components/UserTwo.vue";

export default {
  components: {
    UserOne,
    UserTwo,
  },
};
</script>

<style>
.container {
  width: 100%;
  max-width: 820px;
  margin: 30px auto;
  display: flex;
  gap: 19px;
}
</style>
