<script setup>
import Step from './Step.vue'

defineProps({
    message: {
        type: String,
        default: '',
    }
})
</script>

<template>
    <div class="wizard">
        <h5 class="wizard__title">
            {{ message }}
        </h5>
        <div class="wizard__steps">
            <Step
                :number="'1'"
                :text="'Contacto'"
                :state="true"
            ></Step>
            <Step
                :number="'2'"
                :text="'Directivas'"
                :state="false"
            ></Step>
        </div>
    </div>
</template>

<style>
.wizard {
    margin: 16px 0 24px;
    padding: 24px 24px 0;
}

.wizard__title {
    color: #262626;
    font-family: 'Montserrat', sans-serif;
    font-size: 20px;
    font-weight: 700;
    line-height: 28px;
    margin: 0 0 24px;
    text-align: center;
}

.wizard__steps {
    align-items: center;
    display: flex;
    justify-content: center;
}
</style>