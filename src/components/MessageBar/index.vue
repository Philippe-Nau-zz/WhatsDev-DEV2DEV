<template>
  <div class="message-bar row items-center justify-between">
    <div class="q-mx-md">
      <q-btn
        round
        dense
        unelevated
        icon="lar la-grin-alt"
        text-color="grey"
        size="15px"
        class="q-mr-sm"
      ></q-btn>
      <q-btn
        round
        dense
        unelevated
        icon="las la-paperclip"
        text-color="grey"
        size="15px"
        class="q-mr-sm"
      ></q-btn>
    </div>
    <q-input
      rounded
      outlined
      v-model="text"
      label="Digite uma mensagem..."
      bg-color="white"
      class="input-message"
    ></q-input>
    <q-btn
        round
        dense
        unelevated
        :icon="text != '' ? 'send' : 'fas fa-microphone'"
        text-color="grey"
        size="13px"
        class="q-mr-md"
      ></q-btn>
  </div>
</template>

<script>
export default {
  name: "MessageBar",
  data() {
    return {
      text: "",
    };
  },
};
</script>

<style lang="scss" scoped>

  .message-bar{
    height: 62px;
    background-color: $grey-whats;
  }

  .input-message{
    width: 80%;
  }
</style>