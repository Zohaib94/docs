<script>
export default {
  name: 'HomeCard',
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String
    },
    url: {
      type: String
    },
    description: {
      type: String
    },
    icon: {
      type: String
    }
  }
}
</script>

<template>
  <router-link :to="url" class="home-card-wrapper">
    <section class="home-card" :style="`background-image: url(${icon})`">
      <div class="home-card-content">
        <p class="home-card-title">
          {{ title }}
        </p>
        <p class="home-card-description">
          {{ description }}
        </p>
      </div>
    </section>
  </router-link>
</template>

<style lang="stylus">
@require '../styles/config'

.home-card {
  box-shadow: rgba(0,21,64,.14) 0 2px 6px, rgba(0,21,64,.05) 0 10px 20px;
  border-radius: 20px;
  border: 14px solid #fff;
  background: #fff;
  padding: 10px 0;
  margin-bottom: 20px;
  color: #2c3e50;
  background-repeat: no-repeat;
  background-size: 40px 40px;
  background-position: 15px center;
}

.home-card-content {
  margin-left: 75px;
}

.home-card-description {
  margin-top: 10px;
  text-decoration: none;
}

.home-card-title {
  margin: 0;
  font-size: 1.4rem;
  text-decoration: none;
  font-weight: 600;
}

.home-card-btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: 400;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  border-radius: 3px;
  background-color: $accentColor;
  color: #fff;
}

.home-card-icon {
  width: 40px;
  height: 40px;
  margin-right: 15px;
  padding: 10px;
}

.home-card-wrapper:hover {
  text-decoration: none;
}

@media (min-width: ($MQNarrow + 1px)) {
  .home-card-wrapper {
    flex: 1 1 calc(50% - 30px);
    margin: 0 15px;
  }

  .home-card-wrapper:nth-child(odd) {
    margin-right: 0;
  }

  .home-card-wrapper:nth-child(even) {
    margin-right: 0;
  }
}
</style>
