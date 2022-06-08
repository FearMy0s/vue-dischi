<template>
    <div class="Chose">
        <label class="label" for="typo">Scegli genere </label>
        <select class="select-option" name="typo" id="typo" v-model="Chose.selected">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Metal">Metal</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
        </select>
    </div>
</template>

<script>
import Chose from '../commons/Chose'
export default {
    data() {
        return {
            Chose,
        }
    },
}
</script>

<style lang="scss" scoped>
.Chose {
    display: flex;
    justify-content: center;
    }   
    .label {
        color: var(--primary-color-text);
        text-transform: uppercase;
        font-size: 15px;
        color: white;
    }
    .select-option {
        margin-left: 20px;
        padding: 10px;
}
</style>