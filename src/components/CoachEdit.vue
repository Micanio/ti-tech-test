<template>
    <button @click="showCoachEdit = !showCoachEdit">Edit</button>
    <div class="coach-edit" v-if="showCoachEdit">
        <label for="coach">
        <select name="coach" id="coach">
            <option value="coach1">Laura McGregor</option>
            <option value="coach2">Lana Orton</option>
            <option value="coach3"> hello test</option>
        </select>
        </label>
        <button>Save</button>
    </div>
</template>

<script>

export default {
    name: 'CoachEdit',
    data() {
        return {
            showCoachEdit: false
        }
    }
}

</script>