<template>
    <div class="mapContainer">
        <h2 class="title">Temas etmek</h2>
        <div class="map">
            <div>
                <p class="start">4.8</p>
                <p class="address">FEVZİ ÇAKMAK-2 S 37/20, Kızılay</p>
                <p class="email">epicbookjourney@gmail.com</p>
            </div>
            <div style="width: 100%;">
                <iframe width="100%" height="400" frameBorder="0" scrolling="no" marginHeight="0" marginWidth="0"
                    src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=FEVZ%C4%B0%20%C3%87AKMAK-2%20S%2037/20,%20K%C4%B1z%C4%B1lay+(My%20Business%20Name)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
                    allowFullScreen />
            </div>
        </div>
    </div>
</template>

<style scoped>
.mapContainer {
    padding: 0 5% 160px;
}

.map {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 30px;
}

.title {
    color: #14452f;
font-family: inherit;    font-size: 32px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;

    margin-bottom: 40px;
}

.start {
    position: relative;
    margin-left: 25px;
}

.start::before {
    content: '';
    position: absolute;
    width: 23px;
    height: 22px;
    background-image: url('/img/star.svg');
    background-size: cover;
    background-repeat: no-repeat;

    top: 40%;
    left: -25px;
    transform: translateY(-50%);
}

.address,
.email,
.start {
    color: #1f0e4d;

    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    margin-bottom: 20px;
}

@media (max-width: 1000px) {
    .map {
        flex-direction: column;
    }

    .mapContainer {
        padding: 0 5% 80px;
    }
}
</style>