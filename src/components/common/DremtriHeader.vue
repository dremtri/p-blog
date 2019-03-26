<template>
    <div class="header">
        <div class="logo">
            <span>{{logo}}</span>
        </div>
        <nav>
            <a>
                <span>首页</span>
            </a>
            <a>
                <span>首页</span>
            </a>
            <a>
                <span>首页</span>
            </a>
        </nav>
        <div class="search-box">
            <Input placeholder="Enter text" style="width: auto">
                <Icon type="ios-search" slot="suffix" />
            </Input>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DremtriHeader',
  data () {
    return {
      logo: 'Dremtri'
    }
  }
}
</script>

<style scoped>
.header {
    display: flex;
    background-color: #3286C4;
    height: 3.5rem;
    width: 100%;
    color: #C8CBD1;
    font-size: 1.1rem;
}
.logo {
    flex: 0 0 7.142rem;
    cursor: pointer;
    line-height: 1.4rem;
    padding: 1.07rem;
}
nav {
    flex: 1;
    height: 100%;
}
nav > a {
    cursor: pointer;
    display: inline-block;
    text-decoration:none;
    color: #E6EEF7;
    line-height: 1.4rem;
    padding: 1.07rem;
}
nav > a:hover {
    color: #1A0E89;
    border-bottom: 4px solid #1A0E89;
    height: 3.5rem;
}
.search-box {
    flex: 0 0 14.285rem;
    cursor: pointer;
    line-height: 3.5rem;
}
</style>
