<template>
  <section id='author' class="author">
    <div class="block">
        <img class="img" alt="author" src="/img/author.png" />

      <div class="textBlock">
        <p class="name">Mehmet Kaya</p>
        <p class="text">
          Bir gün, kağıt ve kalemle oturup hayatımı planlamaya karar verdim. Planlama ve Organizasyon becerileri,
          hayatımızdaki karmaşıklıkları düzenlemek için vazgeçilmezdir. Motivasyon ve Güven kazanarak, her şeyin
          üstesinden gelebileceğimizi fark ettim. Hedef Belirleme sürecinde, her adımı dikkatlice planlamak ve organize
          etmek, başarıya giden yolda bize rehberlik eder. Planlarımızı yaparken, her ayrıntıyı düşünmek ve her
          olasılığı hesaba katmak, bizi daha emin adımlarla ilerletir. Bu süreçte, kendimize olan güvenimizi artırarak,
          hedeflerimize ulaşmamız kolaylaşır.

        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.author {
  padding: 0 5% 160px;
}

.img {
  width: 486px;
  height: 558px;
  object-fit: cover;
  object-position: center;
}

.title {
  color: #0b579d;
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
  align-items: stretch;
  flex-direction: row-reverse;
}

/* .imageWrapper {
  position: relative;
  width: 486px;

} */

.textBlock {
  flex-grow: 1;
  padding: 106px 5% 100px;
  background: #f1f1f1;
}

.name {
  color: #333;
  font-family: inherit;
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 23px;
}

.text {
  color: #333;
  font-family: inherit;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  max-width: 613px;
}

.img {
  object-fit: cover;
  object-position: center;
  width: 100%;
}

@media (max-width: 1000px) {
  .author {
    padding: 0 5% 80px;
  }

  .block {
    flex-direction: column-reverse;
  }

  .imageWrapper {
    width: 100%;
    height: 300px;
  }

  .textBlock {
    padding: 20px 5%;
  }

  .text,
  .name {
    max-width: 100%;
    text-align: center;
  }

  .img {
    height: 500px;
  }
}


@media (max-width: 600px) {
  .img {
    height: 300px;
  }
}
</style>