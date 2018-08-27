<template lang='pug'>
  .drawer-content
    .info
      md-avatar.md-large
        img(src='~/assets/images/avatar.jpg', alt='Georgy Yuriev')
      .md-title
        | Георгий Юрьев
        span.md-caption web developer
        md-subheader.location
          md-icon person_pin_circle
          | Москва, Россия
    md-list
      md-list-item
        md-icon view_carousel
        span.md-list-item-text Проекты
      md-divider
      md-list-item.messengers-btns
        md-button.md-icon-button.md-raised.tg-color-bg(:href="telegramLink")
          md-icon.fab.fa-telegram-plane
        md-button.md-icon-button.md-raised.whatsapp-color-bg(:href="whatsappLink")
          md-icon.fab.fa-whatsapp
        md-button.md-icon-button.md-raised(:href="emailLink")
          md-icon mail_outline
        md-button.md-icon-button.md-raised(:href="telephoneLink")
          md-icon call
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

<style lang='scss' scoped>
@import "~vue-material/dist/theme/engine"; // Import the theme engine
@include md-register-theme("default", (theme: dark));
@import "~vue-material/dist/theme/all"; // Apply the theme
.drawer-content {
  position: relative;
  .info {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
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
}
</style>
