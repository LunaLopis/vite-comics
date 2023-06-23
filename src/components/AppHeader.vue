
<script>
export default {
    data() {
        return {
            links: [
                {
                    label: 'Character',
                    href: '#',
                    active: false
                },
                {
                    label: 'Comics',
                    href: '#',
                    active: false
                },
                {
                    label: 'Movies',
                    href: '#',
                    active: false
                },
                {
                    label: 'Tv',
                    href: '#',
                    active: false
                },
                {
                    label: 'Games',
                    href: '#',
                    active: false
                },
                {
                    label: 'Collectible',
                    href: '#',
                    active: false
                },
                {
                    label: 'Videos',
                    href: '#',
                    active: false
                },
                {
                    label: 'Fans',
                    href: '#',
                    active: false
                },
                {
                    label: 'News',
                    href: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    href: '#',
                    active: false
                }
            ]
        }
    },
    methods: {
        setActiveLink(index) {
            this.links.forEach(link => {
                link.active = false;
            });
            this.links[index].active = true;
        }
    },
}
</script>


<template lang="">
    <header class="container d-flex justify-between">
        <a href="/" class="brand ">
            <img class="logo" src="../assets/img/dc-logo.png" alt=" DC Comics" >
        </a> 
        <nav>
            <ul class="navbar" >
                <li v-for="(link, index) in links" :key="index">
                   <a class="font-size" :href="link.href" :class="{ 'active': link.active }" @click="setActiveLink(index) "> {{ link.label.toUpperCase() }}</a>
                </li>
            </ul>
        </nav>      
    </header>
    <div>
        <div class=" container-dark"> 
        <div class="jambotron">
            <button class="text-white">current series</button>
        </div>    
    </div>
    </div>
</template>



<style lang="scss" scoped>
.active {
    border-bottom: 5px solid blue;
    color: blue;
}

header {
    align-items: center;
    padding: 10px;
}

.navbar {
    color: red;
}

.font-size {
    font-size: small;
    font-weight: 900;
}

.logo {
    max-width: 60px;
}

li {
    display: inline-block;
    font-size: 20px;
    padding-left: 20px;

    a {
        padding: 0px 0px 55px 10px;
    }

    :hover {
        border-bottom: 5px solid blue;
        color: blue;
    }
}

.jambotron {
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    height: 250px;
}
</style>