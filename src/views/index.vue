<template>
  <div class="app-container home">
    <CanvasBac />
    <el-row :gutter="20" stype="line-height:20px;margin-bottom:40px">
      <el-col :sm="24" :lg="24">
        <el-card class="card item1" onmouseover="this.style.color='#409EFF'" onmouseout="this.style.color='#000000'">
          <el-col>
            <div class="card left" style="margin: 20px; margin-bottom: 30px">
              <div class="item1-main-content">
                <div style="margin-left: 20px">
                  <h1 style="font-weight: 400; margin: 5px 0">欢迎登录！</h1>
                  <span>两岸猿声啼不住，轻舟已过万重山。</span>
                  <br>
                </div>
              </div>
            </div>
          </el-col>
        </el-card>
      </el-col>
    </el-row>

    <el-row :gutter="20">
      <el-col :sm="24" :lg="12" style="padding-left: 20px">
        <h2>雪菲后台管理框架</h2>
        <p>
          前段时间一直想自己设计golang 项目，但苦于没有很好的思路，于是几个好兄弟向我推荐了java的ruoyi项目。出于对大佬的仰慕，在对系统功能和架构进行了分析之后，利用字节的Hertz 和 Kitex框架采用了完全不同的技术栈和架构设计了它的Golang版本。欢迎大家一起进行技术讨论，承诺开源1年后更改证书为MIT开放给个人及企业免费使用。
        </p>
        <p>
          <b>当前版本:</b> <span>v{{ version }}</span>
        </p>
        <p>
          <el-button
            size="mini"
            icon="el-icon-s-home"
            plain
            @click="goTarget('https://github.com/user823/Sophie/tree/main')"
          >访问主页</el-button>
        </p>
      </el-col>

      <el-col :sm="24" :lg="12" style="padding-left: 50px">
        <el-row>
          <el-col :span="12">
            <h2>技术选型</h2>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <h4>后端技术</h4>
            <ul>
              <li>Hertz</li>
              <li>Kitex</li>
              <li>Etcd</li>
              <li>Gorm</li>
              <li>Opentelemetry</li>
              <li>Minio</li>
              <li>RocketMQ</li>
              <li>...</li>
            </ul>
          </el-col>
          <el-col :span="6">
            <h4>前端技术</h4>
            <ul>
              <li>Vue</li>
              <li>Vuex</li>
              <li>Element-ui</li>
              <li>Axios</li>
              <li>Echarts</li>
              <li>Quill</li>
              <li>...</li>
            </ul>
          </el-col>
        </el-row>
      </el-col>
      <el-col :sm="24" :lg="12" style="padding-left: 50px;transform: scale(0.5)">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>捐赠支持</span>
          </div>
          <div class="body">
            <img src="@/assets/images/pay.jpg" alt="donate" width="100%"/>
            <span style="display: inline-block; height: 30px; line-height: 30px">你可以请作者喝杯咖啡表示鼓励</span>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>

</template>

<script>
export default {
  name: "Index",
  data() {
    return {
      // 版本号
      version: "1.0",
    };
  },
  methods: {
    goTarget(href) {
      window.open(href, "_blank");
    },
  }
};
</script>

<style scoped lang="scss">
.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}
</style>

