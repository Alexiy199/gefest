<script setup>
const getSrcImg = (name) => {
    return `gefest/${name}.jpg`
}
</script>

<template>
    <section id="start-page">
        <div class="wraper-content">
            <div class="wrap-slider">
                <div class="wrap-slide-box" id="txt-show">
                    <article class="start-txt">
                        <h1 class="title">Gefest</h1>
                        <h2 class="sub-title">натяжные потолки</h2>
                        <p>
                            Натяжные потолки любой сложности и дизайна. Поможем воплотить в жизнь
                            Ваши самые смелые идеи. Гарантия качества и надёжности. Индивидуальный
                            подход к каждому клиенту.
                        </p>
                    </article>
                </div>
                <div class="wrap-slide-box" id="example-show">
                    <div class="box-img" id="slide-1">
                        <img :src="getSrcImg('exmp_1')" alt="img" class="img-slide" />
                    </div>
                    <div class="box-img" id="slide-2">
                        <img :src="getSrcImg('exmp_2')" alt="img" class="img-slide" />
                    </div>
                    <div class="box-img" id="slide-3">
                        <img :src="getSrcImg('exmp_3')" alt="img" class="img-slide" />
                    </div>
                    <div class="box-img" id="slide-4">
                        <img :src="getSrcImg('exmp_4')" alt="img" class="img-slide" />
                    </div>
                    <div class="box-img" id="slide">
                        <img :src="getSrcImg('exmp_5')" alt="img" class="img-slide" />
                    </div>
                </div>
            </div>

            <div class="banner-btn">
                <a href="#about" class="start-link">О нас</a>
                <a href="#case-page" class="start-link">примеры</a>
            </div>
        </div>
    </section>
</template>

<style scoped>
.wraper-content {
    background: url('../gefest/exmp_4.jpg') hsl(0, 0%, 15%) no-repeat;
    background-position: center;
    background-size: cover;
    & .banner-btn {
        width: 15em;
        padding: 1em;
        background-color: #00000070;
        border-radius: 10px;
        margin: 0.7em auto;
        & .start-link {
            display: block;
            font-size: 1.5em;
            color: white;
            margin: 0 auto;
        }
    }
}

.start-txt {
    background-color: var(--bg-article);
    margin: 1em;
    padding: 0.4em;
    border: 1px solid black;
}

.wrap-slider {
    width: 98%;
    display: flex;
    flex-direction: row;
    overflow: hidden;
    padding: 5px;
    & .wrap-slide-box {
        position: relative;
        width: 50%;
        align-content: center;
        padding: 2px;
        margin: 0;
        & .box-img {
            min-width: 100%;
            min-height: 100%;
            overflow: hidden;
            scroll-snap-align: start;
            background-color: #00ad0050;
            & .img-slide {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: center;
                aspect-ratio: 1 / 1;
                image-rendering: crisp-edges;
                border: 1px solid black;
                pointer-events: none;
            }
        }
    }
}

#txt-show {
    padding: 1em;
}

@media (width < 946px) {
    .wrap-slider {
        flex-direction: column;
        margin: 1px auto;
        padding: 2px;
        & .wrap-slide-box {
            width: 78%;
            margin: 1px auto;
            & .start-txt {
                width: 100%;
                height: fit-content;
                margin: 0.3em;
                padding: 0.2em;
            }
        }
    }

    .wraper-content {
        & .banner-btn {
            padding: 3px;
            margin: 2px auto;
        }
    }

    #txt-show {
        width: 99%;
        margin: 0;
        padding: 2px;
    }
}

#example-show {
    display: flex;
    gap: 5px;
    overflow-x: auto;
    scroll-behavior: smooth;
    scroll-snap-type: x mandatory;
}

#example-show::-webkit-scrollbar {
    visibility: hidden;
}

#example-show::-webkit-scrollbar-thumb {
    opacity: 0.5;
}
</style>
