<script>
    export default { 
        data() { 
            return { 
                isActive: false 
                }; 
            }, 
            methods: { 
                toggleClass() { 
                    this.isActive = !this.isActive; 
                } 
            } 
        } 
</script>

<template>
    <header>
        <nav class="navigation">
            <div class="navigation__links__popup-dark" :class="{ active: isActive }"></div>
            <div class="container">
                <div class="navigation__wrap">
                    <div class="navigation__wrap-logo">
                        <img src="/img/logo.svg" alt="logo">
                    </div>
                    <ul class="navigation__list-dt">
                        <li class="navigation__list-item">
                            <a href="#" class="navigation__list-item-link">Возможности</a>
                        </li>
                        <li class="navigation__list-item">
                            <a href="#" class="navigation__list-item-link">Как это работает?</a>
                        </li>
                    </ul>
                    <div class="header__burger-btn" :class="{ active: isActive }" @click="toggleClass">
                        <span></span> <span></span> <span></span>
                    </div>                    
                </div>
                <div class="navigation-mb" :class="{ active: isActive }">
                    <ul class="navigation-mb__list">
                        <li class="navigation-mb__list-item">
                            <a href="#" class="navigation__list-item-link">Возможности</a>
                        </li>
                        <li class="navigation-mb__list-item">
                            <a href="#" class="navigation__list-item-link">Как это работает?</a>
                        </li>
                    </ul>
                    <p>г Сургут, ул Базовая, д. 34, офис 10
                        <br> ОГРН 1238600001200 
                        <br> ИНН 8602309464
                        <br><br>ООО Дотсолюшн © 2023
                    </p>
                    
                </div>
            </div>
            
        </nav>
    </header>
</template>

<style scoped>

</style>
