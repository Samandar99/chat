<template>
  <div class="container">
    <UserOne @openModal="getOpenModal" :messageUsers="messageUsers"/>
    <UserTwo @openModal2="userTwoOpen" />
  </div>
  <Modal v-if="isOpenModal" @closeModal="isCloseModal" />
</template>

<script>
import UserOne from "@/components/UserOne.vue";
import UserTwo from "@/components/UserTwo.vue";
import Modal from "@/components/Modal.vue";
export default {
  components: {
    UserOne,
    UserTwo,
    Modal,
  },
  data() {
    return {
      isOpenModal: "",
      messageUsers: [
        { message: "Привет. Как дела? Где ты" },
        { message: "Привет. Как дела? Где ты" },
        { message: "hello" },
        { message: "hi" },
        { message: "Good" },
      ],
    };
  },
  methods: {
    getOpenModal(opens) {
      this.isOpenModal = opens;
    },
    isCloseModal(isclose) {
      this.isOpenModal = isclose;
    },
    userTwoOpen(open2) {
      this.isOpenModal = open2;
    },
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
