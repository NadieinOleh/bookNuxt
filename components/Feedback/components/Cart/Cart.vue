<template>
    <div :class="['cart', flex ? 'cartFlex' : 'cartWidth']">
        <div className={styles.infoBlock} class="infoBlock">
            <img alt="foto" :src="src" />

            <div>
                <p className={styles.name} class="name">{{ name }}</p>
                <p className={styles.age} class="age">{{ age }}</p>
            </div>
        </div>

        <p className={styles.text} class="text">{{ text }}</p>

        <NuxtLink className={styles.link} class="link" to="./">
            daha fazla detay
        </NuxtLink>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    name: {
        type: String,
        required: true
    },
    age: {
        type: String,
        required: true
    },
    text: {
        type: String,
        required: true
    },
    src: {
        type: String,
        required: true
    },
    flex: {
        type: Boolean,
        default: false
    }
})
</script>

<style scoped>
.cart {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    background: #f1f1f1;

    padding: 14px 24px 40px;
}

.cartFlex {
    flex-grow: 1;
}

.cartWidth {
    max-width: 334px;
}

.infoBlock {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 15px;

    margin-bottom: 28px;
}

.name {
    color: #232323;
    font-family: inherit;
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;

    margin-bottom: 9px;
}

.age {
    color: #181818;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

.text {
    font-family: inherit;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    margin-bottom: 36px;
}

.link {
    color: #fe4747;
    font-family: inherit;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

.link:hover {
    color: #14452f;
}

.img {
    width: 78px;
    height: 78px;
}

@media (max-width: 800px) {
    .cartWidth {
        max-width: 100%;
    }
}
</style>