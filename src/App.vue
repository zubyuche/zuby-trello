<script>
import Header from "./components/HeaderSection.vue";
import TheList from "./components/List.vue";
import AddList from "./components/AddnewList.vue";
import Card from "./components/Card.vue";

export default {
  components: {
    "the-header": Header,
    "the-list": TheList,
    "add-list": AddList,
    "the-card": Card,
  
  },
  data() {
    return {
      listItems: [
        {
          ListId: 1,
          title: "To Do",
        },
      ],
      
      nextListId: 2,
      newListTitle: "List Title",
      nextCardId: 2,
      newCardContent: "Enter your content",
      boardTitle: "Project Title",
      inputVisible: false,
      titleVisible: false,
    };
  },
  methods: {
    addNewList() {
      this.listItems.push({
        id: this.nextListId++,
        title: this.newListTitle,
      });
    },
    selectInput() {
      this.inputVisible = !this.inputVisible;
      this.titleVisible = !this.titleVisible;
    },
  },
};
</script>

<template>
  <the-header></the-header>
  <h1 @click="selectInput" :class="{ disable: titleVisible }">
    {{ boardTitle }}
  </h1>
  <input
    type="text"
    placeholder="Enter project title"
    class="disable"
    :class="{ title: inputVisible }"
    @keydown.enter="selectInput"
    v-model="boardTitle"
  />
  <div class="board-container">
    <div class="list-container">
      <the-list v-for="list in listItems" :title="list.title" ></the-list>
      <add-list @click="addNewList"></add-list>
    </div>

  </div>
</template>

<style>
.board-container {
  display: flex;
  margin-left: 20px;
}
.list-container {
  width: 100%;
  height: 100%;
  display: flex;
  gap: 10px;
}
h1 {
  font-size: 22px;
  color: whitesmoke;
  padding-left: 25px;
  cursor: pointer;
}
.title {
  display: inline;
  padding: 5px;
  margin: 10px 10px 10px 25px;
  border: none;
  font-size: 22px;
  height: 20px;
  background: none;
  color: #fff;
  border: none;
  box-shadow: none;
}
</style>