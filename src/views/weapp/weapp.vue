<style lang="less">
.f-title {
  font-size: 20px;
  font-weight: 400;
  margin: 12px 0;
}
.f-p {
  margin: 5px;
  font-size: 14px;
}
.weapp {
  display: flex;
  height: 60px;
  align-items: center;
  justify-content: center;
}
</style>
<template>
  <div>
    <Col>
      <Card>
        <Alert type="warning" show-icon>说明：全新重构设计微信小程序，现已开源！后端即将在XBoot中开发</Alert>
        <div class="weapp">
          <Poptip trigger="hover" title="打开微信扫一扫">
            <div slot="content">
              <img src="https://i.loli.net/2019/10/06/yrtuPTL9DXQUvd2.jpg" width="180px" />
            </div>
            <Button
              type="primary"
              icon="md-qr-scanner"
              shape="circle"
              size="size"
              style="margin-right:20px;"
            >微信扫码体验</Button>
          </Poptip>
          <Button
            to="https://www.bilibili.com/video/av70226175"
            target="_blank"
            shape="circle"
            icon="ios-videocam"
            size="size"
            style="margin-right:20px;"
          >小程序宣传视频</Button>
          <Button
            to="https://github.com/Exrick/xmall-weapp"
            target="_blank"
            shape="circle"
            icon="logo-github"
            size="size"
          >Github地址</Button>
        </div>
        <Row type="flex" justify="start">
          <Col span="6">
            <img src="https://i.loli.net/2019/07/08/5d22e3df51b3b41948.png" width="270px" />
          </Col>
          <Col span="6">
            <img src="https://i.loli.net/2019/07/08/5d22e3def39a024428.png" width="270px" />
          </Col>
          <Col span="6">
            <img src="https://i.loli.net/2019/07/08/5d22e3df6ee8d14238.png" width="270px" />
          </Col>
          <Col span="6">
            <img src="https://i.loli.net/2019/07/08/5d22e3df80a8539956.png" width="270px" />
          </Col>
        </Row>
      </Card>
    </Col>
  </div>
</template>

<script>
export default {
  name: "flutter",
  data() {
    return {};
  },
  methods: {
    init() {}
  },
  mounted() {
    this.init();
  }
};
</script>