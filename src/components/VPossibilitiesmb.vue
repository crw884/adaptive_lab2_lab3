<script setup>
import Swiper from 'swiper/bundle';
    window.addEventListener('DOMContentLoaded', () => {

        const resizableSwiper = (breakpoint, swiperClass, swiperSettings, callback) => {
            let swiper;

            breakpoint = window.matchMedia(breakpoint);

            const enableSwiper = function (className, settings) {
                swiper = new Swiper(className, settings);

                if (callback) {
                    callback(swiper);
                }
            }

            const checker = function () {
                if (breakpoint.matches) {
                    return enableSwiper(swiperClass, swiperSettings);
                } else {
                    if (swiper !== undefined) swiper.destroy(true, true);
                    return;
                }
            };

            breakpoint.addEventListener('change', checker);
            checker();
        }

        const someFunc = (instance) => {
            if (instance) {
                instance.on('slideChange', function (e) {
                    console.log('*** mySwiper.activeIndex', instance.activeIndex);
                });
            }
        };

        resizableSwiper(
            '(max-width: 1280px)',
            '.slider',
            {
                loop: true,
                spaceBetween: 32,
                slidesPerView: 1,
                pagination: {
                    el: '.swiper-pagination',
                    clickable: true,
                },
            },
            someFunc
        );
    });
</script>

<template>
<section class="possibilities-mb">
    <div class="container">
        <div class="swiper slider">
            <div class="swiper-wrapper grid">
                <div class="swiper-slide">
                    <div class="possibilities__card-mb possibilities__card-mb_secondary">
                        <div class="possibilities__card-img-wrap-mb">
                            <img src="/img/card1.svg" alt="">
                        </div>
                        <div class="possibilities__card-name-mb"><strong>Общение с классом</strong></div>
                        <div class="possibilities__card-description-mb">
                            Видеосвязь<br>Чат с классом
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="possibilities__card-mb ">
                        <div class="possibilities__card-img-wrap-mb">
                            <img src="/img/card2.svg" alt="">
                        </div>
                        <div class="possibilities__card-name-mb"><strong>Проведение занятий</strong></div>
                        <div class="possibilities__card-description-mb">
                            Презентация файлов<br>Демонстрация экрана
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="possibilities__card-mb possibilities__card-mb_secondary">
                        <div class="possibilities__card-img-wrap-mb">
                            <img src="/img/card3.svg" alt="">
                        </div>
                        <div class="possibilities__card-name-mb"><strong>Посещаемость</strong></div>
                        <div class="possibilities__card-description-mb">
                            Автоматическое<br>отслеживание<br>присутсвующих
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="possibilities__card-mb ">
                        <div class="possibilities__card-img-wrap">
                            <img src="/img/card4.svg" alt="">
                        </div>
                        <div class="possibilities__card-name-mb">
                            <strong>История занятий</strong>
                        </div>
                        <div class="possibilities__card-description-mb">
                            Материалы урока
                        </div>
                    </div>
                </div>
            </div>
            <br><br>
            <div class="swiper-pagination"></div>
        </div>
    </div>
</section>
</template>

<style scoped>

</style>
