<script setup>
defineProps({
    iconUrl: {
        type: String,
        default: '',
    },
    title: {
        type: String,
        default: '',
    },
    text: {
        type: String,
        default: ''
    }
})
</script>

<template>
    <div class="alert">
        <div class="alert__box">
            <div class="alert__icon" v-if="iconUrl">
                <img class="alert__image" :src="iconUrl" alt="">
            </div>
            <div class="alert__content">
                <div class="alert__title">
                    {{ title }}
                </div>
                <div class="alert__text">
                    {{ text }}
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.alert {
    border-color: #297FFF;
    border-radius: 0.75rem;
    border-style: solid;
    border-width: 1px 1px 1px 5px;
    margin-bottom: 1.5rem;
    padding: 1rem;
}

.alert__box {
    align-items: flex-start;
    display: flex;
    gap: 12px;
}

.alert__icon {
    flex: 0 0 auto;
    height: 16px;
    width: 16px;
}

.alert__image {
    display: block;
    height: 100%;
    object-fit: contain;
    object-position: center;
    width: 100%;
}

.alert__content {
    font-family: 'Mulish', sans-serif;
}

.alert__title {
    color: #404040;
    font-size: 1rem;
    font-weight: 700;
    line-height: 1.5rem;
    margin-bottom: 0.25rem;
}

.alert__text {
    color: #262626;
    font-size: 0.875rem;
    font-weight: 600;
    line-height: 1.125rem;
}
</style>