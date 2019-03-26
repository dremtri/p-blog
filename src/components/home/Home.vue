<template>
    <div>
        <div class="carousel mb-15">
            <Carousel :height="carousel.height"
                      :trigger="carousel.trigger"
                      :autoplay="carousel.autoplay"
                      :loop="carousel.loop"
                      @on-change="change"
                      v-model="value2">
                <CarouselItem v-for="item in carousel.data" :key="item.id">
                    <div class="demo-carousel">
                        <img :src="item.url"/>
                    </div>
                </CarouselItem>
            </Carousel>
        </div>
        <article class="main mb-15">
            <div class="change mr-15">
                <section class="box special-recommend">
                    <div class="hot-title">最热内容</div>
                    <div class="hot-content">
                        <ul>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                        </ul>
                    </div>
                </section>
                <section class="box main-content">
                    <div class="hot-title">主区域</div>
                    <div class="hot-content">
                        <ul>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                        </ul>
                    </div>
                </section>
            </div>
            <div class="stable">
                <section class="box">
                    <div class="hot-title">最热内容</div>
                    <div class="hot-content">
                        <ul>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                        </ul>
                    </div>
                </section>
                <section class="box">
                    <div class="hot-title">热门标签</div>
                    <div class="hot-content">
                        <span v-for="tag in hotTags" :key="tag.id">
                            <Tag :checkable="tag.checkable" :name="tag.name" :color="tag.color">{{tag.name}}</Tag>
                        </span>
                    </div>
                </section>
                <section class="box">
                    <div class="hot-title">推荐文章</div>
                    <div class="hot-content">
                        <ul>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                            <li><span>Hello, 树先生</span></li>
                        </ul>
                    </div>
                </section>
            </div>
        </article>
    </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      value2: 0,
      carousel: {
        height: 300,
        trigger: 'hover',
        autoplay: true,
        loop: true,
        data: [
          {
            id: 1,
            url: require('@/assets/image/carousel/1.jpg')
          },
          {
            id: 2,
            url: require('@/assets/image/carousel/2.jpg')
          },
          {
            id: 3,
            url: require('@/assets/image/carousel/3.jpg')
          },
          {
            id: 4,
            url: require('@/assets/image/carousel/4.jpg')
          }
        ]
      },
      hotTags: [
        {
          id: 1,
          name: 'primary',
          color: 'primary',
          checkable: true
        },
        {
          id: 2,
          name: 'success',
          color: 'success',
          checkable: true
        },
        {
          id: 3,
          name: 'warning',
          color: 'warning',
          checkable: true
        },
        {
          id: 4,
          name: 'volcano',
          color: 'volcano',
          checkable: true
        },
        {
          id: 5,
          name: 'magenta',
          color: 'magenta',
          checkable: true
        },
        {
          id: 6,
          name: 'cyan',
          color: 'cyan',
          checkable: true
        }
      ]
    }
  },
  methods: {
    change (oldValue, value) {
    }
  }
}
</script>

<style scoped>
.carousel {
    height: 21.428rem;
}
.main {
    display: flex;
    flex-flow: row;
    padding: 0 1.071rem;
}
.stable {
    flex: 0 0 21.428rem;
}
.stable > section:last-child {
    margin-bottom: 0
}
.change {
    flex: 1;
}
.special-recommend {
    width: 100%;
}
.hot-title {
    font-size: 1.142rem;
    border-bottom: 1px solid #EEEEEE;
    position: relative;
    color: #2d8cf0;
    padding: 8px 0;
    margin-bottom: 15px;
}
.hot-title:after {
    position: absolute;
    width: 65px;
    height: 2px;
    content: '';
    background: #2d8cf0;
    left: 0;
    bottom: 0;
    transition: width .5s ease;
}
.hot-title:hover:after {
    width: 80px;
}
</style>
