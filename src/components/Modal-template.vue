<template>
    <div class="backdrop" @click.self="closeModal">
        <div :class="styleClass">  
            <slot></slot>       
        </div>
    </div>
</template>

<script>
export default {
    props: [ 'styleClass' ],
    methods: {
        closeModal() {
            this.$emit('close')
        }
    }
}
</script>

<style scoped>
    .newsletter {
        width: 20%;
        max-width: 400px;
        height: 70%;
        max-height: 675px;
        padding: 50px;
        margin: 50px auto;
        background:  rgba(255, 255, 255, 0);
    }
    .modal {
        width: 20%;
        max-width: 400px;
        height: 70%;
        max-height: 675px;
        padding: 50px;
        margin: 50px auto;
        background:  white;
    }
    .backdrop {
        top: 0;
        position: fixed;
        background-color: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
    h2, p {
        margin: 40px;
    }
    form {
        display: inline-block;
        align-content: left;
    }
    label {
        margin: 40px;
    }
</style>