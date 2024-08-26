<template>
    <footer id='footer'  class="footer">
        <a href="./">
            <img class="img" src="/img/Bookd.svg" alt="logo" />
        </a>

        <div  class="block">
            <nav className={styles.nav}>
                <a href="./"  class="link">
                    Ana sayfa
                </a>
                <a href="#author" class="link">
                    Hakkımızda
                </a>
                <a href="#order"  class="link">
                    Temas etmek
                </a>
            </nav>

            <div  class="addressText">
                <p>Adres: FEVZİ ÇAKMAK-2 S 37/20, Kızılay

                </p>
                <p>Telefon: +90 532 123 4567</p>
                <p>E-posta: info@yourrestaurantdesign.com</p>
            </div>

            <div  class="form">
                <Form />
            </div>

            <nav>
                <ul  class="privacyBlock">
                    <li>
                        <p  class="texxt">©2024DRStudio</p>
                    </li>
                    <li>
                        <NuxtLink  class="link" to="/privacy">
                            Gizlilik Politikası
                        </NuxtLink>
                    </li>
                    <li>
                        <NuxtLink  class="link" to="/cookie"> Çerez Kullanımı
                        </NuxtLink>
                    </li>
                </ul>
            </nav>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;

    padding: 160px 5%;

    background: #F1F1F1;
}

.img {
    height: 38px;
    width: 165px;
}

.block {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 50%;
}

.nav {
    display: flex;
    gap: 32px;

    margin-bottom: 50px;
}

.link {
    color: #232323;
    text-align: center;
    font-family: inherit;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

.link:hover {
    color: #14452f;
}

.addressText {
    color: #232323;
    font-family: inherit;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    margin-bottom: 30px;
}

.form {
    align-self: flex-start;

    margin-bottom: 100px;
}

.privacyBlock {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 12px;
}

.text {
    color: #232323;
    font-family: inherit;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

@media (max-width: 1520px) {
    .block {
        width: 70%;
    }
}

@media (max-width: 1000px) {
    .footer {
        flex-direction: column;
        align-items: center;
        gap: 30px;

        padding: 80px 5%;
    }

    .block {
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;

        width: 100%;
    }

    .form {
        align-self: center;
        margin-bottom: 40px;
    }
}

@media (max-width: 800px) {
    .form {
        width: 100%;
    }
}

@media (max-width: 610px) {

    .nav,
    .privacyBlock {
        flex-direction: column;
    }

    .privacyBlock {
        gap: 30px;
    }
}
</style>