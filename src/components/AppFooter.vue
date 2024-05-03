<script>
export default {

}
</script>

<template>
    <div class="footer">
        <span class="button"><a href="">SIGN UP NOW</a></span>
        <div class="footer-list">
            <span><a href="">FOLLOW US</a></span>
            <ul>
                <li><a href=""><img src="../assets/img/footer-facebook.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
                <li><a href=""><img src="../assets/img/footer-periscope.png" alt=""></a></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;
    
.footer {
    @include flex(row, space-around, center);
    background-color: $black;
    height: 15vh;
    position: relative;
    z-index: 1;
    font-family: sans-serif;
    font-size: 1.4rem;
    font-weight: 700;
    gap: 100px;
    

    .button a {
        padding: 10px 15px;
        border: 3px solid $blue;
        color: $white;
    }

    .footer-list a {
        color: $blue;
    }

    .footer-list,
    ul {
        @include flex(row, space-around, center);
    }

    li {
        width: 20%;
        padding-left: 20px
    }
};

</style>