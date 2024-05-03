<script setup>
    const cards = [
        {   
            img:
            {
                src: "/img/card1.svg",
                alt: ""
            },
            card:
            {
                name: "Общение с классом",
                desc1: "Видеосвязь",
                desc2: "Чат с классом",
                desc3: ""
            }
        },
        {   
            img:
            {
                src: "/img/card2.svg",
                alt: ""
            },
            card:
            {
                name: "Проведение занятий",
                desc1: "Презентация файлов",
                desc2: "Демонстрация экрана",
                desc3: ""
            }
        },
        {   
            img:
            {
                src: "/img/card3.svg",
                alt: ""
            },
            card:
            {
                name: "Посещаемость",
                desc1: "Автоматическое",
                desc2: "отслеживание",
                desc3: "присутсвующих"
            }
        },
        {   
            img:
            {
                src: "/img/card4.svg",
                alt: ""
            },
            card:
            {
                name: "История занятий",
                desc1: "Материалы урока",
                desc2: "",
                desc3: ""
            }
        }
        
    ]
</script>

<template>
    <section class="possibilities">
        <div class="container">
                <h2>Возможности</h2>
                <div class="row">
                    <div class="col-3" 
                         v-for="(item, index) in cards" :key="index">
                        <div class="possibilities__card">
                            <div class="possibilities__card-img-wrap">
                                <img :src="item.img.src" :alt="item.img.alt">
                            </div>
                            <div class="possibilities__card-name">
                                <strong>{{ item.card.name }}</strong>
                            </div>
                            <div class="possibilities__card-description">
                                {{ item.card.desc1 }}<br>{{ item.card.desc2 }}<br>{{ item.card.desc3 }}
                            </div>
                        </div>
                    </div>
                </div>
        </div>
    </section>
</template>

<style scoped>

</style>