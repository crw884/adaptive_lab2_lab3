<script setup>
    const ideas = [
        {   
            img:
            {
                src: "/img/schedule.png",
                alt: "schedule"
            },
            card:
            {
                name: "Составьте расписаниe",
                descrition: "Выберите время, предмет и класс. Ученики получат уведомление о предстоящем уроке."
            }
        },
        {   
            img:
            {
                src: "/img/docpdfppt.png",
                alt: "docs"
            },
            card:
            {
                name: "Подготовьте материал",
                descrition: "Загружайте необходимые материалы к уроку."
            }
        },
        {   
            img:
            {
                src: "/img/idcnote.png",
                alt: "notes"
            },
            card:
            {
                name: "Начните урок с учениками",
                descrition: "Задавайте вопросы и вызывайте «к доске» детей с поднятой рукой."
            }
        }
    ]
</script>

<template>
    <section class="ideas">
        <div class="container">
            <h2>Как это работает?</h2>
            <div class="row">
                <div class="col-lg-4"
                     v-for="(item, index) in ideas" :key="index">
                    <div class="ideas__card">
                        <div class="ideas__card-img-wrap">
                            <img :src="item.img.src" :alt="item.img.alt">
                        </div>
                        <div class="ideas__card-name">
                            <p>{{item.card.name}}</p>
                        </div>
                        <div class="ideas__card-description">
                            {{item.card.descrition}}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>

</style>