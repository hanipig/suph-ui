<template>
  <button :class="['suph-button', type ? [type + '-button'] : '', size ? [size + '-button'] : '', {
    disabled: disabled,
    round: round,
    plain: plain
  }]" :disabled="disabled" @click="handleClick">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "SuphButton",
  props: {
    type: {
      type: String,
      default: ""
    },
    size: {
      type: String,
      default: ""
    },
    disabled: {
      type: Boolean,
      default: false
    },
    round: {
      type: Boolean,
      default: false
    },
    plain: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    handleClick () {
      console.log("click");
    }
  }
}

</script>

<style lang="less" scoped>
@primaryColor: #409eff;
@primaryHoverColor: #66b1ff;
@successColor: #67c23a;
@successHoverColor: #85ce61;
@warningColor: #e6a23c;
@warningHoverColor: #ebb563;
@dangerColor: #f56c6c;
@dangerHoverColor: #f78989;
@infoColor: #909399;
@infoHoverColor: #a6a9ad;

.suph-button {
  font-size: 14px;
  padding: 12px 20px;
  text-align: center;
  line-height: 1;
  outline: none;
  background: #ffffff;
  border: 1px solid #dcdfe6;
  box-sizing: border-box;
  border-radius: 4px;
  cursor: pointer;
  color: #606266;
  transition: 0.1s;
  margin: 0;
  white-space: nowrap;
  &:hover,
  &:focus {
    color: #409eff;
    border-color: #c6e2ff;
    background-color: #ecf5ff;
  }
  &:active {
    border-color: @primaryColor;
  }
}

.primary-button {
  color: #ffffff;
  background-color: @primaryColor;
  border-color: @primaryColor;
  &:hover,
  &:focus {
    color: #ffffff;
    background-color: @primaryHoverColor;
    border-color: @primaryHoverColor;
  }
  &:active {
    color: #ffffff;
    background-color: @primaryColor;
    border-color: @primaryColor;
  }
}

.success-button {
  color: #ffffff;
  background-color: @successColor;
  border-color: @successColor;
  &:hover,
  &:focus {
    color: #ffffff;
    background-color: @successHoverColor;
    border-color: @successHoverColor;
  }
  &:active {
    color: #ffffff;
    background-color: @successColor;
    border-color: @successColor;
  }
}

.warning-button {
  color: #ffffff;
  background-color: @warningColor;
  border-color: @warningColor;
  &:hover,
  &:focus {
    color: #ffffff;
    background-color: @warningHoverColor;
    border-color: @warningHoverColor;
  }
  &:active {
    color: #ffffff;
    background-color: @warningColor;
    border-color: @warningColor;
  }
}

.danger-button {
  color: #ffffff;
  background-color: @dangerColor;
  border-color: @dangerColor;
  &:hover,
  &:focus {
    color: #ffffff;
    background-color: @dangerHoverColor;
    border-color: @dangerHoverColor;
  }
  &:active {
    color: #ffffff;
    background-color: @dangerColor;
    border-color: @dangerColor;
  }
}

.info-button {
  color: #ffffff;
  background-color: @infoColor;
  border-color: @infoColor;
  &:hover,
  &:focus {
    color: #ffffff;
    background-color: @infoHoverColor;
    border-color: @infoHoverColor;
  }
  &:active {
    color: #ffffff;
    background-color: @infoColor;
    border-color: @infoColor;
  }
}

// 大小
.medium-button {
  padding: 10px 20px;
  font-size: 14px;
  border-radius: 4px;
}
.small-button {
  padding: 9px 15px;
  font-size: 12px;
  border-radius: 3px;
}
.mini-button {
  padding: 7px 15px;
  font-size: 12px;
  border-radius: 3px;
}

// 禁用
.disabled {
  cursor: not-allowed;
}

.disabled.suph-button {
  color: #c0c4cc;
  background-color: #fff;
  border-color: #ebeef5;
}

.disabled.primary-button {
  color: #fff;
  background-color: #a0cfff;
  border-color: #a0cfff;
}

.disabled.warning-button {
  color: #fff;
  background-color: #f3d19e;
  border-color: #f3d19e;
}

.disabled.info-button {
  color: #fff;
  background-color: #c8c9cc;
  border-color: #c8c9cc;
}

.disabled.success-button {
  color: #fff;
  background-color: #b3e19d;
  border-color: #b3e19d;
}

.disabled.danger-button {
  color: #fff;
  background-color: #fab6b6;
  border-color: #fab6b6;
}

// 圆形按钮
.round {
  border-radius: 20px;
}

//朴素按钮
.plain {
  &:hover,
  &:focus {
    background: #fff;
    border-color: #409eff;
    color: #409eff;
  }
}

.plain.primary-button {
  color: #409eff;
  background: #ecf5ff;
  border-color: #b3d8ff;
  &:hover,
  &:focus {
    color: #ffffff;
    background: @primaryColor;
    border-color: @primaryColor;
  }
  &:active {
    color: #ffffff;
    background: #3a8ee6;
    border-color: #3a8ee6;
    outline: none;
  }
}

.plain.success-button {
  color: #67c23a;
  background: #f0f9eb;
  border-color: #c2e7b0;
  &:hover,
  &:focus {
    color: #ffffff;
    background: @successColor;
    border-color: @successColor;
  }
  &:active {
    color: #ffffff;
    background: #5daf34;
    border-color: #5daf34;
    outline: none;
  }
}

.plain.danger-button {
  color: #f56c6c;
  background: #fef0f0;
  border-color: #fbc4c4;
  &:hover,
  &:focus {
    color: #ffffff;
    background: @dangerColor;
    border-color: @dangerColor;
  }
  &:active {
    color: #ffffff;
    background: #dd6161;
    border-color: #dd6161;
    outline: none;
  }
}

.plain.info-button {
  color: #909399;
  background: #f4f4f5;
  border-color: #d3d4d6;
  &:hover,
  &:focus {
    color: #ffffff;
    background: @infoColor;
    border-color: @infoColor;
  }
  &:active {
    color: #ffffff;
    background: #82848a;
    border-color: #82848a;
    outline: none;
  }
}

.plain.warning-button {
  color: #e6a23c;
  background: #fdf6ec;
  border-color: #f5dab1;
  &:hover,
  &:focus {
    color: #ffffff;
    background: @warningColor;
    border-color: @warningColor;
    outline: none;
  }
  &:active {
    color: #ffffff;
    background: #cf9236;
    border-color: #cf9236;
    outline: none;
  }
}
</style>