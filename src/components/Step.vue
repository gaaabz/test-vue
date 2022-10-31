<script setup>
defineProps({
    number: {
        type: String,
        default: '',
    },
    text: {
        type: String,
        default: '',
    },
    state: {
        type: Boolean,
        default: false
    }
})
</script>

<template>
    <div class="step" :class="{ active: state }">
        <div class="step__box">
            <div class="step__number">
                {{ number }}
            </div>
            <div class="step__text">
                {{ text }}
            </div>
        </div>
    </div>
</template>

<style>
.step {
    display: flex;
    justify-content: center;
    position: relative;
    width: 140px;
}

.step:before {
    content: '';
    display: block;
    height: 2px;
    position: absolute;
    top: 50%;
    transform: translateX(-50%);
    width: 50%;
}

.step__number {
    align-items: center;
    background-color: #F1EAFD;
    border-radius: 100%;
    display: flex;
    font-family: 'Roboto', sans-serif;
    font-size: 16px;
    height: 32px;
    justify-content: center;
    line-height: 16px;
    margin: 0 auto 16px;
    text-align: center;
    width: 32px;
}

.step__text {
    color: #444;
    font-family: 'Montserrat', sans-serif;
    font-size: 16px;
    font-weight: 500;
    margin: 0 auto;
    text-align: center;
}

.step.active .step__number {
    background-color: #722AE9;
    color: #FFF;
}

.step.active .step__text {
    color: #262626;
    font-weight: 700;
}
</style>