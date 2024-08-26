<template>
    <form class="form" @submit="handleSubmit" ref="formRef">
        <input class="input" type="text" id="name" v-model="formData.name" placeholder="Isim" required />
        <input type="email" id="posta" class="input" v-model="formData.email" placeholder="E-posta" required />
        <button class="submit" type="submit">Emir</button>
    </form>
</template>

<script setup>
import { ref } from 'vue';


const router = useRouter();
const formRef = ref(null); 

const formData = ref({
    name: '',
    email: ''
});

const handleSubmit = (e) => {
    e.preventDefault();


    router.push('/thank-you');


    resetForm();
}

const resetForm = () => {
    formRef.value.reset();

}
</script>


<style scoped>
.form {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 18px;
}

.input {
    width: 218px;
    height: 48px;
    border-radius: 10px;
    border: 1px solid #14452f;

    color: #232323;

    font-size: 20px;
    font-style: normal;
    font-weight: 400;


    outline: none;

    padding-left: 23px;
}

.input::placeholder {
    color: rgba(35, 35, 35, 0.6);
    font-family: inherit;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

}

.input:hover::placeholder {
    color: #14452f;
}

.submit {
    width: 218px;
    height: 48px;
    flex-shrink: 0;

    border-radius: 10px;
    background: #14452f;

    color: #fff;
    font-family: inherit;
    font-size: 18px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;

    border: 1px solid transparent;
}

.submit:hover {
    background: #fff;
    border: 1px solid #14452f;
    color: #14452f;
}

@media (max-width: 800px) {
    .form {
        flex-direction: column;
    }

    .submit,
    .input {
        width: 100%;
    }
}
</style>