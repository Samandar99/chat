<template>
  <div class="userOne-block">
    <div class="userone__header">
      <div class="user">
        <img src="@/assets/images/user1.svg" alt="" />
        <div>
          <h4 class="user__name">Александр</h4>
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
        <p class="text">salom</p>
        <span>9:00</span>
      </div>
    </div>
    <div class="footer__input">
      <input
        v-model="inputUserOne"
        class="input"
        type="text"
        placeholder="Написать сообщение..."
      />
      <img
        lass="icon"
        v-if="inputUserOne.length > 0"
        src="@/assets/images/send.svg"
        alt=""
      />
      <img v-else class="icon" src="@/assets/images/photos.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputUserOne: "",
    };
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
.flo {
  float: right;
}
.set {
  font-size: 14px;
  color: #fff;
}
.user__text-one {
  padding: 5px;
  background: #c4bfff;
  border-radius: 15px 15px 15px 0px;
  max-width: 80%;
  word-wrap: break-word;
  display: flex;
  flex-direction: column;
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

.main-chat {
  display: flex;
  align-items: center;
  gap: 5px;
}

.main-chat:nth-child(even) {
  justify-content: flex-end;
}
.main-chat:nth-child(odd) {
  justify-content: flex-start;
}

.text {
  max-width: 60%;
  background: #c4bfff;
  border-radius: 15px 15px 15px 0px;
  padding: 5px;
}
.text1 {
  max-width: 60%;
  background: #d0dcff;
  border-radius: 15px 15px 0px 15px;
  padding: 5px;
}
.icon {
  cursor: pointer;
  width: 20px;
  height: 20px;
  object-fit: contain;
}
</style>