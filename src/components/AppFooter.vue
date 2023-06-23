
<script>
export default {
    data() {
        return {
            contacts: [
                {
                    icon: '/img/footer-facebook.png',
                    href: '#',
                    active: false
                },
                {
                    icon: '/img/footer-twitter.png',
                    href: '#',
                    active: false
                },
                {
                    icon: '/img/footer-youtube.png',
                    href: '#',
                    active: false
                },
                {
                    icon: '/img/footer-pinterest.png',
                    href: '#',
                    active: false
                },
                {
                    icon: '/img/footer-periscope.png',
                    href: '#',
                    active: false
                },
            ]
        }
    }
}
</script>


<template lang="">
    <div class="sfondoNero">
        <div class="container  text-white d-flex justify-between">
        <div class="">
            <button class="first-button">SIGN-UP NOW!</button>
        </div>
        <div class="d-flex">
            <div>
                <button class="follow-button" >FOLLOW US</button>
            </div>
            <ul class="icons-list">
                <li  v-for="(contact, index) in contacts" :key="index">
                  <a :href="contact.href">
                   <img :src="contact.icon" alt="Contact Icon">
                  </a>
                </li>
            </ul>
        </div>
    </div>
    </div>
</template>


<style lang="scss" scoped>
.sfondoNero {
    background-color: #302f2f;
    padding: 20px;
    position: fixed;
    bottom: 0;
    width: 100%;
}

.first-button {
    border: 2px solid rgb(5, 160, 238);
    padding: 10px;
    background-color: #302f2f;
    color: white;
}

.icons-list {
    display: inline-block;
}

li {
    display: inline-block;
}

.follow-button {
    border: 2px solid rgb(5, 160, 238);
    padding: 10px;
    color: rgb(5, 160, 238);
    border: none;
    background-color: #302f2f;
}
</style>