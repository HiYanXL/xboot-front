<style lang="less">
@import "./singleWindow.less";
</style>
<template>
  <div>
    <Card>
      <div slot="title">
        <a @click="close" class="back-title">
          <Icon type="ios-arrow-back" style="margin: 0 0 2px 0" />返回
        </a>
      </div>
      <Form ref="form" :model="form" :label-width="90" :rules="formValidate">
        <FormItem label="名称" prop="name">
          <Input v-model="form.name" style="width: 400px" />
        </FormItem>
        <Form-item>
          <Button
            @click="handleSubmit"
            :loading="submitLoading"
            type="primary"
            style="margin-right:5px"
          >提交并保存</Button>
          <Button @click="handleReset">重置</Button>
        </Form-item>
      </Form>
    </Card>
  </div>
</template>

<script>
export default {
  name: "add",
  data() {
    return {
      loading: true, // 表单加载状态
      submitLoading: false, // 表单提交状态
      form: {
        id: "",
        name: ""
      },
      // 表单验证规则
      formValidate: {
        name: [{ required: true, message: "不能为空", trigger: "blur" }]
      }
    };
  },
  methods: {
    init() {},
    handleReset() {
      this.$refs.form.resetFields();
    },
    handleSubmit() {
      this.$refs.form.validate(valid => {
        if (valid) {
          // this.postRequest("请求路径", this.form).then(res => {
          //   this.submitLoading = false;
          //   if (res.success) {
          //     this.$Message.success("添加成功");
          //     this.submited();
          //   }
          // });
          // 模拟成功
          this.submitLoading = false;
          this.$Message.success("添加成功");
          this.submited();
        }
      });
    },
    close() {
      this.$emit("close", true);
    },
    submited() {
      this.$emit("submited", true);
    }
  },
  mounted() {
    this.init();
  }
};
</script>