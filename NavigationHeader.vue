<template>
    <div class="navigation-header">
        <div class="home-logo"><img src="../assets/home-logo.svg" alt="" /></div>
        <div class="search-bar">
            <GlobleSearch />
        </div>
        <div class="bill-to-info">
            <div>
                <p>Bill To</p>
                <p>Not Selected</p>
            </div>
        </div>
        <div class="ship-to-info">
            <div>
                <p>Ship To</p>
                <p>Not Selected</p>
            </div>
        </div>
        <div class="contact">
            <div>
                <p>Contact</p>
                <p>Not Selected</p>
            </div>
        </div>
        <div class="user-authentication-info">
            <div class="order-info">
                <p>Contact</p>
                <span>Items</span>
                <div class="close-delete-button">
                    <button>Close</button>
                    <button>Delete</button>
                </div>
            </div>
            <div class="authentication">
                <img src="../assets/Down-arrow.svg" alt="" />
                <span>Invaraju</span>
                <img src="../assets/Down-arrow.svg" alt="" />
            </div>
        </div>
        <!-- logo -->
        <!-- search bar -->

        <!-- bill to -->
        <!-- ship to -->
        <!-- contact -->
        <!-- order -->
        <!-- user info{avatar,name ,login and logout} -->
    </div>
</template>
  
<script>
import GlobleSearch from '@/components/GlobleSearch.vue';
export default {
    name: "NavigationHeader",
    props: {
        msg: String
    },
    components: { GlobleSearch }
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.navigation-header {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    height: 113px;
    color: #fff;
    background-color: #3C3C3C;
   p{
    font-size: 16px;
    font-weight: 600px;
    line-height: 10px;
   }
    .home-logo {
        width: 200px;
        padding: 0 16px;
    }

    .search-bar {
        flex: 3;
        padding-right: 54px;
    }

    .bill-to-info {
        flex: 1;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        border-right: 1px solid #656565;
    }

    .ship-to-info {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        flex: 1;
        border-right: 1px solid #656565;
        height: 100%;
    }

    .contact {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        flex: 1;
        border-right: 1px solid #656565;
        height: 100%;
    }

    .user-authentication-info {
        display: flex;
        justify-content: center;
        flex: 2;
        height: 100%;

        .order-info {
            flex: 1;
            height: 100%;
            margin-top:10px;
            span{
                font-size: 14px;
                line-height: 19px;
            }
            .close-delete-button{
                margin-top:-10px;
            }
        }

        .authentication {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            // flex-direction: column;
        }
    }
}

@media screen and (max-width:1400px) {
    .navigation-header {
        height: 80px;
        background-color: #3C3C3C;
    }
}

@media screen and (max-width:1200px) {
    .navigation-header {
        height: 80px;
        background-color: #3C3C3C;
    }
}
</style>
  