<script>
export default {
    data() {
        return {
            comics: [
                {
                title: "Characters",
                },
                {
                title: "Comics",
                },
                {
                title: "Movies",
                },
                {
                title: "Tv",
                },
                {
                title: "Games",
                },
                {
                title: "Videos",
                },
                {
                title: "News",
                },
            ],
            
            shop: [
                {
                    title: "Shop Dc",
                },
                {
                    title: "Shop Dc Collectibles",
                },
            ],

            dc: [
                {
                title: "Term Of Use",
                },
                {
                title: "Privacy policy(New)",
                },
                {
                title: "Ad Choices",
                },
                {
                title: "Advertising",
                },
                {
                title: "Jobs",
                },
                {
                title: "Subscriptions",
                },
                {
                title: "Talent WorkShops",
                },
                {
                title: "CPSC Certificates",
                },
                {
                title: "Ratings",
                },
                {
                title: "Shop Help",
                },
                {
                title: "Contact Us",
                },
            ],
            
            sites: [
                {
                title: "DC",
                },
                {
                title: "MAD Magazines",
                },
                {
                title: "DC Kids",
                },
                {
                title: "DC Universe",
                },
                {
                title: "DC Power Visa",
                },
            ]
        };
    },
}
</script>

<template>
    <section>
        <div class="upper-main">
            --> Content goes here <--
        </div>
        <div class="icon-main">
                icons
        </div>
        <div class="lower-main">
            <div>
                <h3>DC COMICS</h3>
                <ul>
                    <li v-for="item in comics">
                        <a href="">{{ item.title }}</a>
                    </li>
                </ul>
                
                <h3>SHOP</h3>
                <ul>
                    <li v-for="item in shop">
                        <a href="">{{ item.title }}</a>
                    </li>
                </ul>
            </div>
            
            <div>
                <h3>DC</h3>
                <li v-for="item in dc">
                    <a href="">{{ item.title }}</a>
                </li>
            </div>

            <div>
                <h3>SITES</h3>
                <ul>
                    <li v-for="item in sites">
                        <a href="">{{ item.title }}</a>
                    </li>
                </ul>
            </div>
            
            <div>
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/variable" as *;
@use "../style/partials/mixin" as *;
   
section {
    width: 100%;
    .upper-main {
        @include flex(row,start,center);
        background-color: $black;
        height: 15vh;
        padding-left: 200px;
        font-size: 2rem;
    }
        
    .icon-main {
        @include flex(row,start,center);
        padding-left: 200px;
        height: 15vh;
        background-color: $blue;
    }
        
    .lower-main {
        @include flex(row,start,start);
        font-family: sans-serif;
        font-size: 1.1rem;
        padding-left: 200px;
        padding-top: 10px;
        gap: 30px;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        height: 40vh;
        color: $white;
        
        h3 {
            margin: 20px 0;
        };
        
        li {
            margin: 7px 0;
            font-size: 0.8rem; 
        };
        
        a {
            color: $grey;
            &:hover {
                text-decoration: underline;
                color: $white;
            }
        };

        img {
            width: 500px;
            position: absolute;
            top: 400px;
            right: 300px;
        }
    }
}
</style>