<template>
  <section class="cards">
    <div class="flex jc-between">
      <div class="font-14 color-black-light-1">
        <div>
          Available balance
        </div>
        <div class="flex m-t-10 font-bold">
          <div class="cards--currency font-16 bg-green color-white-hard b-r-2">
            S$
          </div>
          <div class="font-20 color-black-hard m-l-10">
            3000
          </div>
        </div>
      </div>
      <div class="cards--new-card-btn color-white-hard b-r-4 font-bold m-t-20">New Card</div>
    </div>
    <div class="cards-details b-r-10">
      <div class="color-green text-align-center font-12 font-bold cursor-pointer">Show card number</div>
      <div class="cards--content">
        <div class="cards--content__list">
          <div class="bg-green padding-20 b-r-10 color-white-hard font-14">
            <div class="text-align-right">
              aspire logo
            </div>
            <div class="m-t-20 font-18 font-bold">
              Mark Henry
            </div>
            <div class="flex letter-spacing-2 font-bold m-t-20">
              <div>
                ****
              </div>
              <div class="m-l-20">
                ****
              </div>
              <div class="m-l-20">
                ****
              </div>
              <div class="m-l-20">
                2020 
              </div>
            </div>
            <div class="flex m-t-10 font-12 letter-spacing-2">
              <div>Thru: 12/20</div>
              <div class="m-l-20 flex">
                CVV: 
                <div class="font-bold m-t-2 m-l-4 font-14">***</div>
              </div>
            </div>
            <div class="text-align-right">
              <img
                src="/visa-logo.png"
                alt="visa-logo"
                width="80px">
            </div>
          </div>
          <div class="options bg-blue-light-4 m-t-40 flex jc-between font-bold">
            <div class="text-align-center">
              <img
                class="b-r-10"
                src="/freeze-icon.jpeg"
                alt="freeze"
                height="20px"
                width="20px">
              <div class="font-12 color-blue-dark-1">
                Freeze Card
              </div>
            </div>
            <div class="text-align-center">
              <img
                class="b-r-10"
                src="/freeze-icon.jpeg"
                alt="freeze"
                height="20px"
                width="20px">
              <div class="font-12 color-blue-dark-1">
                Set Spend limit
              </div>
            </div>
            <div class="text-align-center">
              <img
                class="b-r-10"
                src="/freeze-icon.jpeg"
                alt="freeze"
                height="20px"
                width="20px">
              <div class="font-12 color-blue-dark-1">
                Add to GPay
              </div>
            </div>
            <div class="text-align-center">
              <img
                class="b-r-10"
                src="/freeze-icon.jpeg"
                alt="freeze"
                height="20px"
                width="20px">
              <div class="font-12 color-blue-dark-1">
                Replace card
              </div>
            </div>
            <div class="text-align-center">
              <img
                class="b-r-10"
                src="/freeze-icon.jpeg"
                alt="freeze"
                height="20px"
                width="20px">
              <div class="font-12 color-blue-dark-1">
                Cancel card
              </div>
            </div>
          </div>
        </div>
        <div class="cards--details">
          <transactions title="Card Details" />
          <transactions title="Recent Transactions" class="m-t-20" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  import Transactions from './Transactions.vue'

  export default {
    name: 'Cards',
    components: {
      Transactions
    }
  }
</script>

<style lang="scss" scoped>
  @import '@/variables/utilities';

  .cards {
    margin-left: 25%;
    padding: 60px 40px;

    @include mobile {
      margin: 0;
      padding: 0;
      display: block;
    }

    .cards-details {
      padding: 30px 40px;
      margin-top: 30px;
      box-shadow: 0 0 24px -4px rgba(0, 0, 0, 0.12);
      @include mobile {
        padding: 0;
      }
    }

    &--content {
      display: flex;
      justify-content: space-between;
      margin-top: 10px;

      @include mobile {
        display: block;
      }

      &__list {
        width: 50%;
        @include mobile {
          width: 100%;
        }

        .options {
          padding: 20px 30px;
          border-radius: 10px;

          @include mobile {
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
          }
        }
      }
    }
    &--details {
      width: 50%;
      margin-left: 40px;
      @include mobile {
        width: 100%;
        margin-left: 0;
        margin-top: 20px;
        background: $white-hard;
      }
    }

    &--new-card-btn {
      padding: 5px 10px;
      background: $blue-dark-4;
      @include mobile {
        background: transparent;
        color: $cyan;
        font-size: 14px;
      }
    }
    &--currency { 
      padding: 2px 10px;
    }
  }
</style>