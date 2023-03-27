<template>
  <div class="userOne-block">
    <div class="userone__header">
      <div class="user">
        <img src="@/assets/images/user2.svg" alt="" />
        <div>
          <h4 class="user__name">Евгений</h4>
          <span class="set">Онлайн</span>
        </div>
      </div>
    </div>
    <div class="chat">
      <div class="main-chat">
        <p class="text">Привет. Как дела? Где ты</p>
        <span>9:00</span>
      </div>
      <div class="main-chat">
        <p class="text">Привет. Как дела? Где ты</p>
        <span>9:00</span>
      </div>
    </div>
    <div class="footer__input">
      <input
        v-model="inputUserTwo"
        class="input"
        type="text"
        placeholder="Написать сообщение..."
      />
      <img
        v-if="inputUserTwo.length > 0"
        class="icon"
        src="@/assets/images/send.svg"
        alt=""
      />
      <img
        v-else
        class="icon"
        src="@/assets/images/photos.svg"
        alt=""
        @click="openModal2(true)"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputUserTwo: "",
    };
  },
  methods: {
    openModal2(open2) {
      this.$emit("openModal2", open2);
    },
  },
};
</script>

<style scoped>
.userOne-block {
  max-width: 400px;
  width: 100%;
}

.userone__header {
  background-color: #323232;
  border-radius: 5px 5px 0px 0px;
}

.footer__input {
  background-color: #323232;
  padding: 20px 20px;
  border-radius: 0px 0px 10px 10px;
  display: flex;
  height: 56px;
  justify-content: space-between;
}

.user__name {
  font-size: 18px;
  color: #fff;
}

.user {
  display: flex;
  gap: 10px;
  align-items: center;
  padding: 31px 21px;
}

.set {
  font-size: 14px;
  color: #fff;
}

.chat {
  width: 100%;
  height: 631px;
  background: url(@/assets/images/chatback2.png);
  background-size: cover;
  padding: 10px 10px;
  display: flex;
  flex-direction: column;
  row-gap: 10px;
}

::placeholder {
  color: #fff;
}

.input {
  border: none;
  background: none;
  outline: none;
  color: #fff;
}

.icon {
  cursor: pointer;
  width: 20px;
  height: 20px;
}

.main-chat {
  display: flex;
  align-items: center;
  gap: 5px;
}

.main-chat:nth-child(even) {
  justify-content: flex-start;
}

.main-chat:nth-child(odd) {
  justify-content: flex-end;
}

.text {
  max-width: 60%;
  background: #c4bfff;
  border-radius: 15px 15px 15px 0px;
  padding: 5px;
}
</style>