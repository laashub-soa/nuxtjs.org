<template>
  <div>
    <HomeWelcome />
    <HomeWhy />
    <LazyHomeCompanies />
    <LazyHomeModes />
    <LazyHomeSponsors />
  </div>
</template>

<script>
export default {
  head() {
    const title = this.$i18n.t('homepage.meta.title')
    const description = this.$i18n.t('homepage.meta.description')

    return {
      title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: description
        },
        // Open Graph
        {
          hid: 'og:title',
          property: 'og:title',
          content: title
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: description
        },
        // Twitter Card
        {
          hid: 'twitter:title',
          name: 'twitter:title',
          content: title
        },
        {
          hid: 'twitter:description',
          name: 'twitter:description',
          content: description
        }
      ]
    }
  }
  // async asyncData () {
  //   let sponsors = await fetch('https://opencollective.com/nuxtjs/members/organizations.json').then(res => res.json())
  //   return {
  //     sponsors
  //   }
}
</script>
