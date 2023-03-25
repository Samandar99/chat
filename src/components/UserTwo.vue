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
    <div class="chat"></div>
    <div class="footer__input">
      <input class="input" type="text" placeholder="Написать сообщение..." />
      <img class="icon" src="@/assets/images/photos.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {};
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
  background-color: #fff;
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
}
</style>