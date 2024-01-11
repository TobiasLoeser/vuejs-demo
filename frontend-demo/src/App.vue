<script>
import NewListItemForm from './components/NewListItemForm.vue'
import MyListItem from './components/MyListItem.vue'

export default {
  data() {
    return {
      items: []
    }
  },
  methods: {
    onNewItem(newItem) {
      this.items.push(newItem);
    }
  },
  components: { NewListItemForm, MyListItem }
}
</script>

<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-6 offset-3">
        <h2>New List Item</h2>
        <NewListItemForm @newItem="onNewItem"></NewListItemForm>
        <h2>My list items</h2>
        <ul class="list-group">
          <MyListItem v-for="item in items" :listItem="item"></MyListItem>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
