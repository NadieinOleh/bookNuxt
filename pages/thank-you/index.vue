<script setup>

useHead({
  titleTemplate: '%s - Oleh'
})

</script>

<template>
  <section class="aboutBlock container">
    <div class="textBlock">
      <h1 class="title">Teşekkür ederim </h1>
      <p class="titleText">İsteğin için teşekkürler.</p>

      <Button :text="'Geri'" :isDefault='true' :to="'./'" />
    </div>

    <img className={styles.aboutImg} class="aboutImg" width={548} height={956} src='/img/book.png' alt='thank image' />
  </section>
</template>

<style scoped>
.container {
  padding-inline: 5%;
}

.aboutBlock {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;

  margin-bottom: 160px;
}

.subTitle {
  color: #333;
  font-family: inherit;
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  margin-bottom: 12px;
}

.textBlock {
  display: flex;
  flex-direction: column;

  max-width: 710px;
}

.title {
  color: #14452f;
  font-family: inherit;
  font-size: 60px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  text-transform: uppercase;

  margin-bottom: 25px;
}

.titleText {
  color: #14452f;
  font-family: inherit;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  margin-bottom: 50px;
}

.buttonBlock {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 15px;

  margin-bottom: 170px;
}

.aboutTitle {
  color: #14452f;
  font-family: inherit;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;

  margin-bottom: 12px;
}

.aboutText {
  color: #333;
  text-align: justify;
  font-family: inherit;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.aboutImg {
  object-fit: cover;
  object-position: center;
}

@media (max-width: 1440px) {
  .textBlock {
    max-width: 550px;
  }
}

@media (max-width: 1000px) {
  .aboutBlock {
    flex-direction: column;
    margin-bottom: 80px;
  }

  .textBlock {
    max-width: 100%;
  }

  .titleText,
  .buttonBlock {
    margin-bottom: 30px;
  }

  .aboutImg {
    width: 100%;
    height: 300px;
  }
}

@media (max-width: 610px) {
  .title {
    font-size: 24px;
  }

  .subTitle {
    font-size: 20px;
  }

  .buttonBlock {
    flex-direction: column;
    align-items: normal;
  }
}
</style>