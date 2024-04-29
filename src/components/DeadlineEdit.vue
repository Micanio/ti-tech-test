<template>
    <button @click="showDeadlineEdit = !showDeadlineEdit">Edit</button>
    <div class="deadline-edit" v-if="showDeadlineEdit">
        <label for="deadline">Change deadline:</label>
        <input type="date" name="deadline" id="deadline">
        <button>Save</button>
    </div>
</template>

<script>

export default {
    name: 'DeadlineEdit',
    data() {
        return {
            showDeadlineEdit: false
        }
    }
}

</script>