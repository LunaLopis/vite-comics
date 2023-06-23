
<script>
import img1 from '../assets/img/buy-comics-digital-comics.png'
import img2 from '../assets/img/buy-comics-merchandise.png'
import img3 from '../assets/img/buy-comics-subscriptions.png'
import img4 from '../assets/img/buy-comics-shop-locator.png'
import img5 from '../assets/img/buy-dc-power-visa.svg'
export default {
    data() {
        return {
            links: [
                {
                    label: 'DC COMICS',
                    href: '#',
                    items: ['Characters', 'Comics', 'Movies', 'Tv', 'Games', 'Videos', 'News'],
                    active: false,
                },
                {
                    label: 'DC ',
                    href: '#',
                    items: ['Terms of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificate', 'Rating', 'Shop Help', 'Contact Us'],
                    active: false,
                },
                {
                    label: 'SITES',
                    href: '#',
                    items: ['MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
                    active: false,
                },
                {
                    label: 'SHOP',
                    href: '#',
                    items: ['Shop DC', 'Shop DC', 'Collectibles DC'],
                    active: false,
                },
            ],

            cards: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS '
                },
                {
                    image: img2,
                    text: 'DC MERCHANDISE'
                },
                {
                    image: img3,
                    text: 'SUBSCRIPTION'
                },
                {
                    image: img4,
                    text: 'COMIC SHOP LOCATOR'

                },
                {
                    image: img5,
                    text: 'DC POWER VISA'
                }
            ]
        }
    }
}
</script>


<template lang="">
    <div class="rigaAzzurra">
        <div class="container">
            <div class="row">
                 <div class="col">
                    <div v-for="(card, index) in cards" :key="index" class="card d-flex justify-center">
                         <img class="img-card" :src="card.image" alt="">
                         <!-- <img class="img-card" src="../assets/img/buy-comics-digital-comics.png" alt=""> -->
                         <h3 class="text-white card-text">{{card.text}}</h3>
                    </div>
                 </div>
            </div>

        </div>

    </div>


   <div class="sfondoNero">
      <div class="container text-white d-flex justify-between">
            <div class="d-flex col links">
                <div v-for= "(link, index) in links" :key="index" class="margin text-white ">
                    <h3>{{link.label}}</h3>
                    <ul> 
                    <li v-for="(item, itemIndex) in link.items" :key="itemIndex"  class="text-white font-size" >
                        <a :href="link.href" class="text-white">{{item}}</a>
                    </li>
                    </ul>
                </div>
            </div>

            <div class="col col-2">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>

</template>


<style lang="scss" scoped>
.container-dark {
    background-color: black;

    width: 100%;
}

.rigaAzzurra {
    background-color: rgb(69, 140, 238);
    width: 100%;
}

.sfondoNero {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    width: 100%;
}

img {
    width: 400px;
}

.links {
    padding-top: 30px;
}

ul {
    padding-top: 10px;

}

.font-size {
    font-size: 10px;
}

.margin {
    margin-right: 20px;
}

.col {
    display: flex;
    flex-wrap: wrap;
}

.col-2 {
    justify-content: flex-end;
}

.card {
    width: calc(100% / 5 - 10px);
    padding: 30px;
    display: flex;
    align-items: center;
    margin-right: 10px;
}

.img-card {
    max-width: 50px;
    max-height: 100px;
}

.card-text {
    padding: 10px;
}
</style>