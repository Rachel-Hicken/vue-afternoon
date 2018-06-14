<template>
    <div>
        <form @submit.prevent="submitNewBot">
            <input type="text" placeholder="Bot Name" v-model="botName"/>
            <input type="number" placeholder="Attack Value" v-model="attackValue"/>
            <input type="number" placeholder="Health Value" v-model="healthValue"/>
            <button type="submit">Submit</button>
            <button>Clear</button>
        </form>
    </div>
</template>

<script>
export default {
    props: ["submitNewBot"]
}
</script>

<style>

</style>


