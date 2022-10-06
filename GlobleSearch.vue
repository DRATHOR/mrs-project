<template>
  <div class="globle-search">
    <!-- menu -->
    <button class="search-button" v-on:click="handleClickEvent">

      Option
      <div class="selected-option-and-icon">
        <span class="option-icon">O</span>
        <span class="toggle-arrow">
          <img src="../assets/Down-arrow.svg" alt="" />
        </span>
      </div>

    </button>
    <div class="select-option" v-if="showMenu">
      <div>Open Order</div>
      <div>Customer</div>
      <div>Item</div>
      <div>Part Number</div>
      <div>Vender</div>
      <div>Pruchase</div>
    </div>
    <input type="text" placeholder="Search Customer" class="search-option" />
    <!-- input -->
  </div>
</template>
  
<script>
// import DownArrow from '../assets/Down-arrow.svg'
export default {
  name: 'GlobleSearch',
  props: {
    msg: String
  },
  // components: {
  //   DownArrow
  // },
  data() {
    return {
      showMenu: false,
    }
  },
  methods: {
    handleClickEvent() {
      this.showMenu = !this.showMenu;
    }
  }
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.globle-search {
  position: relative;
  display: flex;
  justify-content: flex-start;
  align-items: center;

  ::-webkit-input-placeholder {
    /* Edge */
    color: #9A9A9A;
    font-size: 16px;
  }

  :-ms-input-placeholder {
    /* Internet Explorer */
    color: #9A9A9A;
    font-size: 16px;
  }

  ::placeholder {
    color: #9A9A9A;
    font-size: 16px;
  }

  .search-button {
    display: flex;
    align-items: center;
    justify-content: center;
    padding:0 16px 0 24px;
    font-weight: 600;
    height: 40px;
    border: none;
    border-radius: 30px 0 0 30px;
    background: #e8e8e8;
    color: #000;
    font-size: 18px;

  }

  .selected-option-and-icon {
    display: flex;
    align-items: center;
    padding-left:8px;
    justify-content: space-around;
    .option-icon {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 24px;
      height: 24px;
      border-radius: 8px;
      background: #5392b5;
      color:#fff;
    }
    .toggle-arrow{
      margin-left:8px;
    }

   
  }
  .select-option {
      position: absolute;
      width:145px;
      display: flex;
      justify-content: flex-start;
      align-items: flex-start;
      flex-direction: column;
      background: #fff;
      box-shadow: 0 0 4px gray;
      padding: 16px;
      top: 48px;
      font-size: 18px;
      color:#69697D;
      line-height: 30px;
      border-radius: 5px;
    }
  .search-option {
    flex: 1;
    height: 40px;
    outline: none;
    border: none;
    padding: 0 16px;
    border-radius: 0 30px 30px 0;
    font-size: 16px;
  }
}
</style>
  