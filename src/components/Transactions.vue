<template>
  <div class="transactions b-r-10">
    <div class="transactions--box bg-blue-light-5 padding-20">
      <div class="color-blue-dark-1 font-12 flex jc-between">
        <div class="flex">
          <img
            class="cursor-pointer"
            src="/transaction.svg"
            alt="transaction"
            width="14px">
          <div class="m-l-10 font-bold">
            {{ title }}
          </div>
        </div>
        <div>
          <img
            @click="toggleView"
            class="cursor-pointer"
            src="/dropdown.svg"
            alt="dropdown"
            width="14px">
        </div>
      </div>
    </div>
    <div class="transactions--option" v-if="show">
      <div class="padding-20 font-12">
        <div class="flex jc-between">
          <div class="flex">
            <div class="height-30 bg-blue-light-4 width-30 b-r-15 flex ai-center jc-center">
              <img
                src="/option.svg"
                alt="visa-logo"
                width="20px"
                height="20px">
            </div>
            <div class="m-l-10">
              <div class="flex jc-between">
                <div class="color-black-hard font-bold">Hamleys</div>
              </div>
              <div class="m-t-2 color-green">
                20 May 2020
              </div>
              <div class="flex m-t-6">
                <div class="transactions--option__box bg-blue-dark-2 b-r-10 flex jc-center ai-center">
                  <img
                    src="/box-logo.jpeg"
                    alt="visa-logo"
                    width="10px">
                </div>
                <div class="color-blue-dark-4 font-10 font-bold m-l-4">Refund on debit card</div>
              </div>
            </div>
          </div>
          <div class="color-green font-bold">+ S$ 150</div>
        </div>
      </div>
      <hr class="transactions--option__border" />
      <div class="padding-20 font-12">
        <div class="flex jc-between">
          <div class="flex">
            <div class="height-30 bg-blue-light-4 width-30 b-r-15 flex ai-center jc-center">
              <img
                src="/option.svg"
                alt="visa-logo"
                width="20px"
                height="20px">
            </div>
            <div class="m-l-10">
              <div class="flex jc-between">
                <div class="color-black-hard font-bold">Hamleys</div>
              </div>
              <div class="m-t-2 color-green">
                20 May 2020
              </div>
              <div class="flex m-t-6">
                <div class="transactions--option__box bg-blue-dark-2 b-r-10 flex jc-center ai-center">
                  <img
                    src="/box-logo.jpeg"
                    alt="visa-logo"
                    width="10px">
                </div>
                <div class="color-blue-dark-4 font-10 font-bold m-l-4">Refund on debit card</div>
              </div>
            </div>
          </div>
          <div class="color-green font-bold">+ S$ 150</div>
        </div>
      </div>
      <hr class="transactions--option__border" />
      <div class="padding-20 font-12">
        <div class="flex jc-between">
          <div class="flex">
            <div class="height-30 bg-blue-light-4 width-30 b-r-15 flex ai-center jc-center">
              <img
                src="/option.svg"
                alt="visa-logo"
                width="20px"
                height="20px">
            </div>
            <div class="m-l-10">
              <div class="flex jc-between">
                <div class="color-black-hard font-bold">Hamleys</div>
              </div>
              <div class="m-t-2 color-green">
                20 May 2020
              </div>
              <div class="flex m-t-6">
                <div class="transactions--option__box bg-blue-dark-2 b-r-10 flex jc-center ai-center">
                  <img
                    src="/box-logo.jpeg"
                    alt="visa-logo"
                    width="10px">
                </div>
                <div class="color-blue-dark-4 font-10 font-bold m-l-4">Refund on debit card</div>
              </div>
            </div>
          </div>
          <div class="color-green font-bold">+ S$ 150</div>
        </div>
      </div>
      <hr class="transactions--option__border" />
      <div class="padding-20 font-12">
        <div class="flex jc-between">
          <div class="flex">
            <div class="height-30 bg-blue-light-4 width-30 b-r-15 flex ai-center jc-center">
              <img
                src="/option.svg"
                alt="visa-logo"
                width="20px"
                height="20px">
            </div>
            <div class="m-l-10">
              <div class="flex jc-between">
                <div class="color-black-hard font-bold">Hamleys</div>
              </div>
              <div class="m-t-2 color-green">
                20 May 2020
              </div>
              <div class="flex m-t-6">
                <div class="transactions--option__box bg-blue-dark-2 b-r-10 flex jc-center ai-center">
                  <img
                    src="/box-logo.jpeg"
                    alt="visa-logo"
                    width="10px">
                </div>
                <div class="color-blue-dark-4 font-10 font-bold m-l-4">Refund on debit card</div>
              </div>
            </div>
          </div>
          <div class="color-green font-bold">+ S$ 150</div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: 'Transactions',
    data () {
      return {
        show: true
      }
    },
    props: {
      title: {
        type: String,
        required: true,
        default () {
          return ''
        }
      }
    },
    methods: {
      toggleView () {
        this.show = !this.show
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '@/variables/utilities';

  .transactions {
    box-shadow: 0 0 24px -4px rgba(0, 0, 0, 0.12);
    @include mobile {
      margin: 20px;
    }

    &--box {
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
    }

    &--option {
      &__box {
        height: 16px;
        width: 16px;
      }
      &__border {
        border: 0.5px solid $gray-light-4;
        width: 80%;
        margin-top: 0;
        margin-bottom: 0;
      }
    }
  }
</style>