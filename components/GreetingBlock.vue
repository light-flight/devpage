<template lang='pug'>
  .greeting-block
    .greeting-block__background
    .greeting-block__content

      md-avatar.md-large
        img(src='~/assets/images/avatar.jpg', alt='Georgy Yuriev')
      .md-title
        | Георгий Юрьев
        span.md-caption web developer
        md-subheader.location
          md-icon person_pin_circle
          | Москва, Россия

      md-list
        md-divider
        md-list-item.one-btn-item
          md-button.greeting-block-mail-btn(:href="emailLink")
            md-icon mail_outline
            span georgy.yuriev@gmail.com
        md-list-item.one-btn-item
          md-button(:href="telephoneLink")
            md-icon call
            | 8 (915) 199-09-22
          md-button.md-icon-button.md-dense(:href="telegramLink")
            md-icon.fab.fa-telegram-plane
          md-button.md-icon-button.md-dense(:href="whatsappLink")
            md-icon.fab.fa-whatsapp

      p.first-word
        | Привет! Я занимаюсь реализацией бизнес-идей в вебе.
        br
        | Люблю делать современные интерфейсы, которыми хочется пользоваться.
</template>

<script>
export default {
  computed: {
    telegramLink () {
      return 'https://t.me/LightFlight'
    },
    whatsappLink () {
      return 'https://api.whatsapp.com/send?phone=79151990922'
    },
    emailLink () {
      return 'mailto:georgy.yuriev@gmail.com'
    },
    telephoneLink () {
      return 'tel:+79151990922'
    }
  }
}
</script>

<style lang='scss'>

@import "~vue-material/dist/theme/engine"; // Import the theme engine
@include md-register-theme("default", (theme: dark));
@import "~vue-material/dist/theme/all"; // Apply the theme

.greeting-block {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.greeting-block__background {
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: url(~/assets/images/3.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  filter: blur(15px) brightness(0.82);
  transform: scale(1.2);
}

.greeting-block__content {
  width: 90%;
  max-width: 600px;
  margin: 0 auto;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  .md-avatar {
    $size: 110px;
    width: $size;
    height: $size;
    margin: 1.25em 0 .75em;
  }
  .md-title {
    margin-top: 0;
    color: #fff;
    text-align: center;
    .md-caption {
      display: block;
      margin-top: 4px;
    }
    .md-icon {
      margin-right: 4px;
      color: inherit !important;
    }
  }
  .md-list {
    background-color: transparent !important;
  }
  .messengers-btns {
    margin-top: 1em;
    .md-button {
      opacity: .85;
      &:hover {
        opacity: 1;
      }
    }
    .md-list-item-content {
      justify-content: center;
    }
  }
  .one-btn-item {
    .md-button {
      margin-top: 0;
      margin-bottom: 0;
    }
  }
  .greeting-block-mail-btn {
    span {
      line-height: inherit;
      text-transform: lowercase;
    }
  }
}
</style>
