<script>
import { store } from '../store'
export default {
    name: "CercaArchetipo",
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div>
        <input type="text" placeholder="Seleziona carte in base all'archetipo" v-model="store.Cerca">
        <button type="submit" @click.prevent="$emite('nomeEmit')">cerca</button>
    </div>
</template>

<script lang="scss" scoped></script>