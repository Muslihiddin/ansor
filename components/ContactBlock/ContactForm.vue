<template>
    <form @submit.prevent="onSubmit">
        <label for="name">Your name</label>
        <input class="rounded-lg px-5 py-5 mt-2 mb-8" type="text" id="name">

        <label for="phone">Your phone number</label>
        <input class="rounded-lg px-5 py-5 mt-2 mb-8" type="number" id="number">

        <label for="text">Text</label>
        <textarea class="rounded-lg px-5 py-5 mt-2 mb-8" name="text" id="text"></textarea>

        <button type="submit" class="rounded-lg flex justify-center items-center px-20 py-6"
         @click="onSubmit"
        >Send</button>
    </form>
</template>

<script>
export default {
    name: 'ContactForm',
    methods: {
        onSubmit() {
            return 1;
        }
    }
}
</script>

<style lang="scss" scoped>
    form {
        border: 2px solid #f1f1f1;
        border-radius: 32px;
        padding: 48px;
        max-width: 590px;
    }

    label {
        font-family: var(--rubik);
        font-weight: 400;
        font-size: 24px;
        line-height: 38px;
        color: var(--Black_01);
    }

    input {
        width: 100%;
        background-color: #f2f2f2;
        outline: none;
    }

    textarea {
        width: 100%;
        min-height: 164px;
        max-height: 200px;
        background-color: #f2f2f2;
        outline: none;
    }

    button {
        background-color: var(--Green_01);
      
        font-family: var(--montserrat);
        font-size: 16px;
        line-height: 24px;
        font-weight: 600;
        color: #fff;

        &:active {
            transform: scale(.9);
        }
    }
    
    @media screen and(max-width: 1050px) {
        form {
            margin-top: 50px;
        }
    }

    @media screen and(max-width: 640px) {
        form {
            border: none;
            width: 100%;
            padding: 10px;
            margin-top: 50px;
        }
    }
</style>