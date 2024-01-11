<script>
export default {
    data() {
        return {
            newItem: ''
        };
    },
    methods: {
        addItem() {
            if (this.newItem) {
                this.$emit('newItem', this.newItem)
                this.newItem = '';
            }
        }
    }
}
</script>

<template>
    <div class="mb-3">
        <input type="text" class="form-control" id="listItem" v-model="newItem" placeholder="New List Item Name"
            @keyup.enter="addItem">
    </div>
    <button type="submit" class="btn btn-primary mb-3" @click="addItem"><i class="bi bi-plus-circle"></i> Add</button>
</template>
