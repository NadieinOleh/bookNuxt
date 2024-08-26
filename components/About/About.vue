<template>
    <section  id="about" class="container aboutBlock">
      <div class="textBlock">
        <p  class="subTitle">
          Bireysel Yaklaşım ve İlerleme Yönetimi: Hayatınızı Düzenleyin ve
          Hedeflerinize Kolayca Ulaşın
        </p>
        <h1  class="title">
          Planlama ve Organizasyon ile Işlerde başarı planlama metodolojisi:
          Hayatınızı Şekillendirin
        </h1>
        <p  class="titleText">
          Mehmet Kaya`nın bu kitabı, başarılı bir hayat için gerekli olan
          Planlama ve Organizasyon becerilerinizi geliştirmenize yardımcı
          oluyor. Kaya, Motivasyon ve Güven unsurlarını ele alarak, hem kişisel
          hem de profesyonel hayatınızda nasıl daha etkili olabileceğinizi
          anlatıyor. Kitap, zaman yönetimi, öncelik belirleme ve etkili planlama
          konularında derinlemesine bilgiler sunuyor. Hedef Belirleme ve
          Adaptasyon stratejileri ile okuyucuların karşılaştıkları zorluklarla
          başa çıkmalarını sağlıyor. Bireysel Yaklaşım ile kendi yolunuzu
          bulmanıza ve bu yolda daha emin adımlarla ilerlemenize yardımcı olacak
          pratik öneriler sunuyor. Bu eser, düzenli ve başarılı bir yaşam sürmek
          isteyen herkes için mükemmel bir rehber. Mehmet Kaya, hayatın her
          alanında başarıya ulaşmanız için gerekli olan araçları ve teknikleri
          bu kitapta sizlerle paylaşıyor.
        </p>

        <div  class="buttonBlock">
            <Button :to="'#form'" :text="'Kitap sipariş et'" :is-default="true"/>
            <Button :to="'/img/Mert_Yıldırım.pdf'" :text="'PDF olarak indir'" :is-default="false"/>
        </div>

        <div>
          <h2 class="aboutTitle">Kitap hakkında</h2>
          <p  class="aboutText">
            Mehmet Kaya, kişisel gelişim ve organizasyon alanında uzman bir
            yazardır. Planlama ve Organizasyon becerilerini geliştirmek
            isteyenler için eşsiz kaynaklar sunan Kaya, bu alanda birçok
            başarılı kitaba imza atmıştır. Kariyeri boyunca, çeşitli şirketlerde
            danışmanlık yaparak, liderlerin ve çalışanların daha etkili
            olabilmeleri için stratejiler geliştirmiştir.
            <br />
            Kaya’nın eserlerinde, Motivasyon ve Güven unsurlarının kişisel ve
            profesyonel yaşamda başarıya ulaşmada nasıl kritik bir rol oynadığı
            vurgulanır. Kitaplarında, Hedef Belirleme ve Adaptasyon stratejileri
            ile okuyucularının karşılaştıkları zorluklarla başa çıkmalarını ve
            değişen koşullara hızlıca uyum sağlamalarını sağlamak için yöntemler
            sunar
            <br /> Mehmet Kaya, aynı zamanda Bireysel Yaklaşım felsefesine
            inanan bir yazardır. Her bireyin kendine özgü bir potansiyeli
            olduğuna ve bu potansiyeli ortaya çıkarmak için kişisel yöntemler
            geliştirilmesi gerektiğine inanır. Kaya’nın kitapları,
            okuyucularının kendi yollarını bulmalarına ve bu yolda daha emin
            adımlarla ilerlemelerine yardımcı olacak pratik öneriler içerir.
            Mehmet Kaya, düzenli ve başarılı bir yaşam sürmek isteyenler için
            vazgeçilmez bir rehberdir.
          </p>
        </div>
      </div>

      <img
  
        class="aboutImg"
        alt="about image"
        width={548}
        height={956}
        src="/img/book.png"
      />

   
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
  font-family: 'inherit';
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  margin-bottom: 12px;
}

.textBlock {
  display: flex;
  flex-direction: column;

  max-width: 1000px;
}

.title {
  color: #14452f;
font-family: 'inherit';
  font-size: 60px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  text-transform: uppercase;

  margin-bottom: 25px;
}

.titleText {
  color: #14452f;
font-family: 'inherit';
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

  margin-bottom: 100px;
}

.aboutTitle {
  color: #14452f;
font-family: 'inherit';
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;

  margin-bottom: 12px;
}

.aboutText {
  color: #333;
  text-align: justify;
font-family: 'inherit';
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.aboutImg {
  object-fit: cover;
  object-position: center;
  align-self: flex-start;
}

@media (max-width: 1440px) {
  .textBlock {
    max-width: 550px;
  }

  .aboutImg {
    width: 400px;
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

  .title {
    font-size: 30px;
  }

  .textBlock {
    max-width: 100%;
  }

  .titleText, .buttonBlock {
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