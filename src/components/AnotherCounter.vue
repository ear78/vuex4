<template>
    <div>
        <button class="btn btn-primary" @click="asyncIncrement({by: 400, duration: 1000})">Increment</button>
        <button class="btn btn-primary" @click="asyncDecrement({by: 50, duration: 200})">Decrement</button>
    </div>
</template>

<script>
    import { mapActions } from 'vuex';

    export default {
        methods: {
            ...mapActions([
                'asyncIncrement',
                'asyncDecrement'
            ])
        }
    }
</script>