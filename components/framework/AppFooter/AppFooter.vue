<template>
  <div class="app-footer">
    <div class="app-footer-cont">
      <div class="social">
        <a target="_blank" href="https://github.com/zhangquanming/nuxt-blog"><i class="iconfont icongithub"></i></a>
        <a target="_blank" href="https://juejin.im/user/448256473565480"><i class="iconfont iconjuejin-logo"></i></a>
        <a target="_blank" href="https://segmentfault.com/u/mingme"><i class="iconfont iconsegmentfault"></i></a>
      </div>

      <div class="contact">
        <span class="cat"> <i class="iconfont iconwangzhi"></i> <a target="_blank" href="#">hello {at} mingme.net</a></span>
        <span class="cat"> <i class="iconfont iconqq"></i>419654548</span>
        <span class="cat"> <i class="iconfont iconyouxiang"></i> <a target="_blank" href="#">419654548@qq.com</a></span>
      </div>

      <div class="copyright">
        <span>Copyright © 2020-2021 Mingme. All Rights Reserved. </span>
        <a target="_blank" href="https://beian.miit.gov.cn/">京ICP备 2020042020号.</a>
        <span class="gwab">
          <a target="_blank" href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010802033443">
            <img src="../../../assets/images/beian_icon.png" />
            <span>京公网安备 11010802033443号</span>
          </a>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style lang="less" scoped>
@keyframes pulse {
  0% {
    transform: scale(0.9);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: scale(1.1);
    opacity: 0;
  }
}
.app-footer {
  position: relative;
  width: 100%;
  height: @heightFooter;
  background-color: #151515;
  color: @colorFooterText;
  .app-footer-cont {
    margin: 0 auto;
    text-align: center;
    .social {
      display: flex;
      justify-content: center;
      align-items: center;
      a {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        color: @colorFooterText;
        transition: all 0.3s;
        width: 36px;
        height: 36px;
        margin: 0 30px;
        border-radius: 50%;
        &:after {
          z-index: 1;
          content: '';
          position: absolute;
          top: 0px;
          bottom: 0px;
          left: 0px;
          right: 0px;
          border-radius: 100%;
          background: transparent;
          border: 1px solid @colorFooterText;
          -webkit-animation: pulse 2s infinite;
          animation: pulse 2s infinite;
        }
        &:hover {
          &:after {
            border-color: @colorTextWhite;
          }
          color: @colorTextWhite;
        }
        i {
          font-size: 24px;
          line-height: 1;
          &:last-child {
            margin-right: 0;
          }
        }
      }
    }
    .contact {
      .cat {
        flex: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 14px;
        font-weight: 400;
        i {
          display: inline-block;
          font-size: 20px;
          margin-right: 10px;
        }
      }
    }
    .copyright {
      border-top: 1px solid @colorTextContent;
      line-height: 40px;
      text-align: center;
      letter-spacing: 1px;
      font-size: 12px;
      font-weight: 400;
      a {
        &:hover {
          color: @colorTextLight;
        }
      }
      .gwab a {
        img {
          vertical-align: sub;
          width: 18px;
          height: 18px;
        }
      }
    }
  }
}
@media only screen and (min-width: @containerMaxWidth-xl) {
  .app-footer {
    padding-top: 50px;
    .app-footer-cont {
      width: 1280px;
      .social {
        margin-bottom: 40px;
      }
      .contact {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 20%;
        margin-bottom: 30px;
      }
    }
  }
}
@media only screen and (min-width: @containerMaxWidth-md) and (max-width: @containerMaxWidth-xl) {
  .app-footer {
    padding-top: 50px;
    .app-footer-cont {
      width: 100%;
      .social {
        margin-bottom: 40px;
      }
      .contact {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 10%;
        margin-bottom: 30px;
      }
    }
  }
}
@media only screen and (max-width: @containerMaxWidth-md) {
  .app-footer {
    padding-top: 20px;
    .app-footer-cont {
      width: 100%;
      .social {
        margin-bottom: 20px;
      }
      .contact {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-bottom: 10px;
        overflow: hidden;
        width: 100%;
        .cat {
          line-height: 24px;
        }
      }
      .copyright {
        line-height: 18px;
        padding: 7px 40px;
      }
    }
  }
}
</style>
