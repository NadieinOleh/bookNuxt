<template>
    <div>
        <component :is="linkComponent" :to="isInternalLink ? to : null" :href="isInternalLink ? null : to"
            :target="isInternalLink ? null : '_blank'">
            <button :class="buttonClasses">{{ text }}</button>
        </component>
    </div>
</template>

<script setup>
import { defineProps, computed } from 'vue';

const props = defineProps({
    to: {
        type: String,
        required: true
    },
    text: {
        type: String,
        required: true
    },
    isDefault: {
        type: Boolean,
        required: true
    },
});

const isInternalLink = computed(() => props.to.startsWith('/') && !props.to.endsWith('.pdf'));
const linkComponent = computed(() => (isInternalLink.value ? 'NuxtLink' : 'a'));

const buttonClasses = computed(() => {
    return ['button', props.isDefault ? 'default' : 'custom'];
});
</script>

<style scoped>
.button {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    min-width: 272px;
    height: 58px;
    width: 100%;
    border-radius: 10px;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    text-align: center;
    font-size: 22px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}

.default {
    background: #14452f;
    color: #fff;
}

.custom {
    background: #fff;
    color: #14452f;
    border: 1px solid #14452f;
    max-width: 272px;
}

.custom:hover {
    color: #488B00;
    border: 1px solid #488B00;
}

.default:hover {
    background: #488B00;
}

@media (max-width: 610px) {
    .custom {
        max-width: 100%;
    }
}
</style>