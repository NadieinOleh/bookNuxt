<template>
    <section  class="feedback">
      <h2  class="title">Yorumlar</h2>

      <div  class="block">
        <Cart
          :src='"/img/card1.png"'
          :name="'Elif A'"
          :age="'23 yıl'"
          :text='textCard1'
          :flex='true'
        />
        <Cart
          :src='"/img/card2.png"'
          :name="'Mehmet K'"
          :age='"55 yıl"'
          :text='textCard2'
          :flex='false'
        />
        <Cart
          :src='"/img/card3.png"'
          :name="'Olivia D'"
          :age='"27 yıl"'
          :text='textCard3'
          :flex='false'
        />
      </div>
    </section>
</template>

<script setup>
 const textCard2 =
  "Bu kitap, hayatımın dönüm noktası oldu. Mehmet Kaya'nın anlatımı ve sunduğu zaman yönetimi metodolojisi sayesinde hedeflerin belirlenmesi ve gerçekleştirilmesi konusunda büyük ilerleme kaydettim. Hedefler yaşamın temel bir unsurudur prensibini gerçekten kavradım. Kesinlikle tavsiye ederim!"
  ;
  const textCard1 =  "Planlama ve Organizasyon Sanatı, sadece iş hayatında değil, kişisel hayatımda da büyük değişiklikler yapmamı sağladı. Motivasyon ve güven kazanmamda çok yardımcı oldu. Kitapta sunulan planlama ve organizasyon teknikleri, günlük yaşamımda daha düzenli ve hedeflerime odaklı olmamı sağladı. Kişisel verimlilik için harika bir kaynak."

  const textCard3 ="Mehmet Kaya'nın yazım tarzı ve verdiği örnekler çok etkileyici. Kitap, hedef belirleme ve organizasyon becerileri konusunda gerçekten rehber niteliğinde. İlerleme yönetimi ve adaptasyon konularında sunduğu bilgiler, hedeflerime ulaşmamda bana büyük ölçüde yardımcı oldu. Profesyonel gelişim için mükemmel."

</script>

<style scoped>
.feedback {
  padding: 0 5% 160px;
}

.title {
  color: #14452f;
 font-family: inherit;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;

  margin-bottom: 40px;
}

.block {
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  gap: 29px;

  border-top: 1px solid #232323;
  padding-top: 44px;
}

@media (max-width: 1000px) {
  .feedback {
    padding: 0 5% 80px;
  }

  .block {
    flex-wrap: wrap;
    justify-content: center;
  }
}

</style>