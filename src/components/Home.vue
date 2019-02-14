<template>
  <el-container>
    <el-header style="height:560px;">
      <el-row style="height:60px;background-color: rgb(32, 49, 96);position:fixed;width:100%;z-index:999;">
        <el-col :span="1" style="width:2.5rem;">&nbsp;</el-col>
        <el-col :span="2"><img src="/static/img/logo.png" alt="" style="padding-top:14px;width: 85px"></div>
        </el-col>
      </el-row>
      <div class="banner">
        <el-carousel height="500px">
          <el-carousel-item v-for="item,index in imgList" :key="index">
            <h3 class="ml50">
              <strong>"{{item.title1}}"</strong>— {{item.title2}}</h3>
            <span class="ml50">{{item.title3}}</span>
          </el-carousel-item>
        </el-carousel>
      </div>
    </el-header>
    <el-main>
      <el-row style="box-shadow: 0 0 10px 0 rgba(122,177,249,.34);">
        <el-col :span="6">
          <div name="5" class="pj-top-list" style="height:329px;">
            <div class="pj-top-bg"><img src="/static/img/h-1.jpg" width="100%" height="100%" class="hover-bg">
              <div class="pj-door"><img src="/static/img/h-1.jpg" class="pj-img">
                <div class="operation">
                  <!-- <button type="button" class="el-button el-button--default"> -->
                  <span>
                    <span class="icon iconfont icon-zhiding"></span>
                  </span>
                  </button>
                </div>
                <div class="pj-info">
                  <div class="pj-logo"><img src="/static/img/wms.png"></div>
                  <div class="introduce">
                    <h2>WMS项目</h2>
                    <p>WMS项目</p> <br>
                    <a class="goMonitor"> 查看详情 → </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </el-col>
      </el-row>
      
      <div  class="pd-main">
        <el-row style="height:70px;">
          <el-col :span="12">
            <div  class="grid-content">
              <h2  class="h2 project-cap">
                <strong  class="bt-border">项目</strong>
                <strong style="margin-left:-8px;">列表</strong>
                <span  class="translate">PROJECT MANAGEMENT</span>
              </h2>
            </div>
          </el-col>
          <el-col :span="12">
          <div style="float:right;">
            <div  class="c-search fr"><input  placeholder="请输入项目名称" class="c-input">
            <el-button type="primary" class="c-search-button position" icon="el-icon-search"></el-button>
            </div>
          </div>
          </el-col>
        </el-row>
        <div style="height:100px;">

        </div>
        <el-pagination
          style="float:right;"
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="currentPage4"
          :page-sizes="[10, 20, 30]"
          :page-size="10"
          layout=" prev, pager, next,sizes,total"
          :total="1">
        </el-pagination>
      </div>

      
    </el-main>
  </el-container>

</template>

<script>
export default {
  data() {
    return {
      radio: "aa",
      imgList: [
        {
          title1: "窥见",
          title2: "大数据实时监控利器",
          title3: "PROJECT MANAGEMENT EXPERTS AROUND YOU"
        },
        {
          title1: "标题",
          title2: "标题1",
          title3: "描述1描述1描述1描述1描述1描述1描述1描述1"
        },
        {
          title1: "标题",
          title2: "标题2",
          title3: "描述2描述2描述2描述2描述2描述2描述2描述2"
        },
        {
          title1: "标题",
          title2: "标题3",
          title3: "描述3描述3描述3描述3描述3描述3描述3描述3"
        }
      ],
      currentPage4: 4
    };
  },
  methods:{
    handleSizeChange(val) {
    },
    handleCurrentChange(val) {
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
.el-header {
  padding: 0 !important;
}
.el-main {
  padding: 0 !important;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}
.banner {
  width: 100%;
  height: 500px;
  background: url("/static/img/banner1.png") center top no-repeat;
  background-size: 100% 100%;
  margin-top: 60px;
}
.banner .ml50 {
  margin-left: 50px;
}
.banner h3 {
  font-size: 34px;
  color: #fff;
  margin-top: 100px;
  position: absolute;
  z-index: 100;
  left: 100px;
  font-family: pingFangSC-Regular;
  opacity: 1;
  font-weight: normal;
}
.banner h3 strong {
  font-size: 43px;
  font-weight: normal;
}
.banner span {
  font-size: 22px;
  color: #fff;
  margin-top: 240px;
  position: absolute;
  z-index: 100;
  left: 100px;
}
.pj-top-list {
  position: relative;
  overflow: hidden;
}
.pj-top-list .pj-top-bg {
  width: 100%;
  height: 100%;
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: 100px auto;
}
.pj-top-list .hover-bg {
  opacity: 0;
  position: absolute;
  z-index: 1;
  transition: all 0.6s cubic-bezier(0.1, -0.6, 0.25, 0.22);
}
.pj-top-list .pj-top-bg .pj-door {
  background: #fff;
  padding: 10% 0;
  width: 100%;
  text-align: center;
  color: #666;
  position: relative;
}
.pj-top-list .pj-top-bg .pj-door .pj-img {
  width: 160px;
  height: 160px;
  display: block;
  margin: 0 auto;
  border-radius: 100%;
  opacity: 1;
}
.pj-top-list .pj-top-bg .pj-door .operation {
  position: absolute;
  z-index: 100;
  right: 25px;
  top: 25px;
  display: none;
}
.pj-top-list .pj-top-bg .pj-door .pj-info {
  cursor: pointer;
  position: relative;
  z-index: 1;
  width: 100%;
}
.pj-top-list .pj-top-bg .pj-door .pj-info .pj-logo {
  bottom: 130px;
}
.pj-top-bg .pj-door .pj-info .pj-logo,
.pj-top-list .pj-top-bg .pj-door .pj-info .pj-logo {
  position: absolute;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  bottom: 140px;
  display: none;
  width: 90px;
  height: 90px;
}
.pj-top-list .pj-top-bg .pj-door .pj-info .pj-logo img {
  width: 100%;
  display: block;
  margin: 0 auto;
}
.pj-top-list .pj-top-bg .pj-door .pj-info .introduce h2 {
  font-size: 22px;
  padding: 30px 0 10px;
  letter-spacing: 2px;
  font-weight: normal;
}
.pj-top-list .pj-top-bg .pj-door .pj-info .introduce p {
  font-size: 14px;
  line-height: 24px;
}
.pj-top-list .pj-top-bg .pj-door .pj-info .introduce .goMonitor {
  cursor: pointer;
  color: #fff;
  font-size: 14px;
  display: none;
}

.pj-all-list:hover .hover-bg,
.pj-top-list:hover .hover-bg {
  opacity: 0.2;
}

.pj-top-list:hover .pj-top-bg {
  background: #7ab1f9;
  transition: all 3s cubic-bezier(0.58, -0.6, 0.25, 0.22);
}

.pj-top-list:hover .pj-top-bg .pj-door {
  background: #7ab1f9;
}

.pj-top-list:hover .pj-top-bg .pj-door .pj-img {
  opacity: 0;
}

.pj-top-list:hover .pj-top-bg .pj-door .operation {
  display: block;
}

.pj-top-list:hover .pj-top-bg .pj-door .pj-info .pj-logo {
  display: block;
  -webkit-transform-origin: center center;
  transform-origin: center center;
  -webkit-animation: animations 0.5s infinite ease-in-out;
  animation: animations 0.5s infinite ease-in-out;
  -webkit-animation-iteration-count: 1;
  animation-iteration-count: 1;
}
@-webkit-keyframes animations {
  0% {
    opacity: 0;
    width: 20px;
  }

  to {
    opacity: 1;
    width: 90px;
  }
}

@keyframes animations {
  0% {
    opacity: 0;
    width: 20px;
  }

  to {
    opacity: 1;
    width: 90px;
  }
}
.pj-top-list:hover .pj-top-bg .pj-door .pj-info .introduce h2 {
  margin-top: -60px;
  color: #fff;
}

.pj-top-list:hover .pj-top-bg .pj-door .pj-info .introduce p {
  color: #fff;
}

.pj-top-list:hover .pj-top-bg .pj-door .pj-info .introduce .goMonitor {
  margin-top: 20px;
  margin-bottom: 5px;
  line-height: 35px;
  display: block;
}

.pj-all-list:hover .pj-top-bg .pj-door .pj-info .introduce .goMonitor {
  margin-top: 10px;
  margin-bottom: 13px;
  line-height: 35px;
  display: block;
}

.pd-main{
  padding-left: 2.5rem;
  padding-right: 2.5rem;
  padding-top: 20px;
  padding-bottom: 60px;
}
.project-cap {
  font-size: 28px;
  color: #333;
}

.project-cap .bt-border {
  border-bottom: 3px solid #7ab1f9;
  padding: 10px 0;
  
}
.project-cap strong{
font-weight: normal;
}

.project-cap .translate {
  font-size: 16px;
  color: #7ab1f9;
  text-align: center;
  font-weight: normal;
}
.c-input {
  background: #fff;
  border: 1px solid hsla(0, 0%, 59%, .2);
  border-radius: 100px;
  height: 24px;
  line-height: 31px;
  padding: 5px 30px;
  color: #333;
  font-size: 14px
}
input::-webkit-input-placeholder {
  color: #e3e3e3
}

input:-moz-placeholder,
input::-moz-placeholder {
  color: #e3e3e3
}

input:-ms-input-placeholder {
  color: #e3e3e3
}
.c-search {
  position: relative;
  overflow: hidden;
  width: 232px;

}

.c-search-button.position {
  position: absolute;
  top: 0;
  right: 0
}

.c-search-button {
  background: #7ab1f9;
  border-radius: 0 30px 30px 0;
  height: 35px;
  text-align: center;
  padding: 0 16px;
  border: 0;
  color: #fff
}

.c-search-button:hover {
  color: #fff;
  background: #3395fb
}

</style>
