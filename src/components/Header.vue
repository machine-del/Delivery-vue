<template>
    <header>
        <div class="container">
            <div class="header-box">
                <router-link class="header-logo logo" to="/"><img src="../assets/images/logo.png" alt="logo"></router-link>
                <div class="header-controls">
                    <button class="btn btn-primary">
                        <img src="../assets/images/icons/user.png" alt="user">
                        Войти
                    </button>
                    <button class="btn btn-outline" @click="openModal()">
                        <img src="../assets/images/icons/shopping-cart.png" alt="cart">
                        Корзина
                    </button>
                </div>
            </div>
        </div>
    </header>
</template>

<script setup>
    const emit = defineEmits(['toggleModal'])
    const openModal = () => {
        emit('toggleModal')
    }
</script>

<style scoped>
header {
    display: flex;
    align-items: center;
    min-height: 124px;
}

.header-box {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.header-controls {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 10px;
}
</style>