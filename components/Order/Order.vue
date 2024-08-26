<template>
    <section id='order' class="order">
        <h2 class="title">Posta yoluyla kitap sipariş etme</h2>
        <p class="text">
            Hedeflerinize ulaşmak için gereken motivasyonu ve güveni kazanın. Bu kitap, planlama ve organizasyon
            becerilerinizi geliştirerek, başarıya ulaşmanızı kolaylaştıracak. Hayatınızı dönüştürmeye bugün başlayın.

        </p>

        <div class="form">
            <Form />
        </div>
    </section>
</template>

<style scoped>
.order {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    background: #f1f1f1;

    padding: 80px 5%;

}

.title {
    color: #232323;

    font-size: 40px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
    text-align: center;

    margin-bottom: 14px;
}

.text {
    color: #232323;
    text-align: center;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    max-width: 1024px;

    margin-bottom: 40px;
}



@media (max-width: 1000px) {
    .order {
        padding: 40px 5%;
    }

    .title {
        font-size: 28px;
    }
}


@media (max-width: 800px) {
    .order {
        align-items: stretch;
    }
}
</style>