<template>
  <div class="conversation-area">
    <Header />
    <div class="card-area">
      <div
        class=" card row items-center justify-between q-px-md"
        v-for="item in 10"
        :key="item"
      >
        <q-avatar size="40px" class="q-mr-sm">
          <img src="https://i.pravatar.cc/40"/>
        </q-avatar>
        <div class="message column justify-around full-height q-pt-sm">
          <div class="row justify-between">
            <div class="column">
              <span>Philippe Nau</span>
              <span v-if="1 == 1">Nova mensagem recebida</span>
              <span v-else>Veja nossa última conversa...</span>
            </div>
            <div class="column items-center justify-center">
              <span>7:41</span>
            </div>
          </div>
          <q-separator></q-separator>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/header";

export default {
  name: "ConversationArea",
  components: {
    Header,
  },
};
</script>

<style lang="scss" scoped>
  .conversation-area {
    height: 100vh;
    width: 410px;
    background-color: #fff;
  }

  .card-area{
    height: calc(100vh - 118px);
    overflow: auto;
  }

  .card{
    background-color: #FFF;
    height: 72px;
    cursor: pointer;
    &:hover{
      background-color: $grey-whats;
    }
  }
  
  .q-avatar{
    flex-grow: 0.1;
  }

  .message{
    flex-grow: 5;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
    width: 250px;

    span:first-child{
      font-size: 16px;
    }
    span:last-child{
      font-size: 12px;
      color: $sub-title-grey;
    }
  }

</style>
