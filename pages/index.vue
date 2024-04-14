<template>
  <div>
    <structure-app-header></structure-app-header>
    <collections-card-find-friend></collections-card-find-friend>
    <collections-quiz-collection :collectionName="'Discover'"></collections-quiz-collection>
    <collections-top-author></collections-top-author>
    <collections-top-collection></collections-top-collection>
    <collections-quiz-collection :collectionName="'Trending Quiz'"></collections-quiz-collection>
    <collections-quiz-collection :collectionName="'Top Picks'"></collections-quiz-collection>
    <structure-app-nav-bottom></structure-app-nav-bottom>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
