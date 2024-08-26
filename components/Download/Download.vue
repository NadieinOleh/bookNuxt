<template>
    <section class="download">
        <h2 class="title">Alıntıyı indir</h2>

        <div  class="block">
            <div  class="img"> </div>

            <div class="textBlock">
                <p  class="subTitle"> Mehmet Kaya</p>
                <h3  class="textTitle">Planlama ve Organizasyon Sanatı</h3>
                <p  class="text">
                    Elif Yılmaz, bu kitabında Bireysel Yaklaşım ve İlerleme Yönetimi
                    konularına odaklanarak kişisel hedeflerinize ulaşmanın en etkili
                    yollarını açıklıyor. Hedef Belirleme sürecinde karşılaşılan
                    zorlukları aşmak için stratejiler sunan Yılmaz, aynı zamanda
                    Motivasyon ve Güven kavramlarını da işliyor. Kitap, okuyucuların
                    kendi güçlü yönlerini keşfetmelerine ve bu yönleri nasıl
                    kullanabileceklerine dair pratik öneriler içeriyor. Planlama ve
                    Organizasyon becerilerinizi geliştirerek, hayatınızdaki
                    karmaşıklıkları düzenleyebilir ve hedeflerinize daha hızlı
                    ulaşabilirsiniz. Kişisel gelişim yolculuğunuzda size rehberlik
                    edecek bu eser, hedeflerinize ulaşmanız için gerekli olan tüm
                    bilgileri ve ipuçlarını sunuyor. Elif Yılmaz, kendi deneyimlerinden
                    yola çıkarak, kişisel başarıya ulaşmanın sırlarını paylaşıyor ve
                    Adaptasyon yeteneklerinizi geliştirmenizi sağlıyor.
                </p>
                <Button :to="'/img/Mert_Yıldırım.pdf'" :text="'PDF olarak indir'" :is-default="false" />
            </div>
        </div>
    </section>
</template>

<style scoped>
.download {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;

    padding: 0 5% 160px;
}

.img {
    width: 414px;
    min-width: 409px;
    height: 570px;

    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 20px;
    background: url('/img/download.png') lightgray 50% / cover no-repeat;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
}

.title {
    color: #14452f;
   font-family: inherit;
    font-size: 32px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;

    margin-bottom: 38px;
}

.block {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: row-reverse;
    gap: 70px;
}

.subTitle {
    color: #333;
   font-family: inherit;
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    margin-bottom: 18px;
}

.textTitle {
    color: #14452f;
   font-family: inherit;
    font-size: 60px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-transform: uppercase;

    margin-bottom: 23px;
}

.text {
   font-family: inherit;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    max-width: 613px;

    margin-bottom: 23px;
}

@media (max-width: 1000px) {
    .download {
        align-items: center;

        padding: 0 5% 80px;
    }

    .block {
        flex-direction: column;
        gap: 40px;
    }

    .title {
        align-self: flex-start;
        font-size: 30px;
    }

    .textTitle {
        font-size: 30px;
    }
}

@media (max-width: 610px) {
    .textTitle {
        font-size: 24px;
    }
}


@media (max-width: 510px) {
    .img {
        width: 100%;
        min-width: 350px;
    }
}
</style>