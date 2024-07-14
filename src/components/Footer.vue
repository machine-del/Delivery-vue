<template>
    <footer>
        <div class="container">
            <div class="footer-box">
                <router-link class="header-logo logo" to="/"><img src="../assets/images/logo.png" alt="logo"></router-link>
                <div class="footer-nav">
                    <ul>
                        <li><a href="goods.html">Ресторанам</a> </li>
                        <li><a href="goods.html">Курьерам</a></li>
                        <li><a href="goods.html">Пресс-центр</a></li>
                        <li><a href="goods.html">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-social">
                    <img src="../assets/images/social/instagram.png" alt="instagram">
                    <img src="../assets/images/social/facebook.png" alt="facebook">
                    <img src="../assets/images/social/vk.png" alt="vk">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
footer {
    display: flex;
    align-items: center;
    min-height: 156px;
    padding: 60px 0px;
}

.footer-box {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 36px;
    flex-wrap: wrap;
}

.footer-nav {
    flex-grow: 1;
}

.footer-nav ul {
    display: flex;
    align-items: center;
    list-style: none;
    padding: 0;
    margin: 0;
    gap: 15px;
    flex-wrap: wrap;
}

.footer-nav ul li {
    color: #595959;
    font-size: 18px;
    font-weight: 400;
}

.footer-nav ul li a {
    text-decoration: none;
    color: #595959;
}

.footer-social {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 20px;
}
</style>