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
    props: {
        elemImage: String,
        elemSeries: String,
        elemType: String,
    },
}
</script>

<template>
    <section>
        <div class="upper-main">
            <div class="card">
                <img :src="elemImage"
                :class="elemType === 'comic book' ? 'comic-book' : 'graphic-novel'">
                <span>{{ elemSeries }}</span>
            </div>
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
    
    .card {
    @include flex(column,space-between,center);
    position: relative;
    z-index: 10;
    color: $white;
    width: calc(100% / 6 - 50px / 6);
    img {
        width: 10vw;
        height: 26vh;
        margin-bottom: 10px;
    }
    .comic-book{
        border:1px solid red;
    }
    .graphic-novel{
        border:1px solid green;
    }
    span{
        display: inline-block;
        height: 30px;
        font-family: sans-serif;
        font-size: 10px;
    }
    span,img{
        align-self: flex-start;
    }
}
}
</style>