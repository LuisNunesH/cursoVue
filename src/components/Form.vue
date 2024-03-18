<template>
    <form action="">
        <div>
            <InputText />
        </div>
</form>
</template>
<script>
    import InputText from './InputText.vue';

    export default{
        name: 'Form',
        components: {
            InputText,
        }
    }
</script>