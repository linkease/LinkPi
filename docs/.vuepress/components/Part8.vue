<template>
    <div class="part8">
        <div class="part8_imgs">
            <img class="part8_bj" :src="P8_bg1" loading="lazy" />
            <img :src="P8_front1" alt class="part8_img" loading="lazy" />
        </div>
        <div class="text_info3" title="保姆式向导配置，支持拨号、旁路由等各种模式">保姆式向导配置，支持拨号、旁路由等各种模式</div>

        <div class="part8_content max-width">
            <div class="content_text">
                <div class="text_tit" title="更简单的Openwrt">更简单的Openwrt</div>
                <div
                    class="text_info"
                    title="iStore应用市场，插件安装卸载就是这么轻松。DDNSTO，一个浏览器搞定内网穿透，远程访问Openwrt、远程终端、远程桌面..."
                >
                    iStore应用市场，插件安装卸载就是这么轻松。
                    <br />DDNSTO，一个浏览器搞定内网穿透，远程访问Openwrt、远程终端、远程桌面...
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import P8_bg1 from "../public/home/P8_bg1.png"
import P8_front1 from "../public/home/P8_front1.png"
import P8_bg2 from "../public/home/P8_bg2.png"
import P8_front2 from "../public/home/P8_front2.png"
export default {
    data() {
        return {
            P8_bg1,
            P8_front1,
            P8_bg2,
            P8_front2
        }
    }

}
</script>

<style lang="scss" scoped>
* {
    -webkit-box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
    box-sizing: border-box;
    word-wrap: break-word;
    outline: none;
}
.part8 {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    background: linear-gradient(189.9deg, #000000 28.89%, #000000 129.1%);
    position: relative;
    .max-width {
        max-width: 1440px;
    }
    .part8_imgs {
        .part8_bj {
            background-size: cover;
            width: 100%;
            height: 100%;
            z-index: 0;
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;
            top: 0;
        }
        .part8_img {
            position: relative;
            width: 100%;
            margin-top: 100px;
        }
    }
    .text_info3 {
        position: relative;
        height: 60px;
        font-family: IBM Plex Mono;
        font-style: normal;
        font-weight: bold;
        font-size: 24px;
        line-height: 60px;
        color: #aca8ff;
        z-index: 999;
        font-size: 2vw;
        top: -2vw;
    }

    .part8_content {
        flex: 0 0 100%;
        max-width: 100%;
        position: absolute;
        z-index: 999;
        margin-top: 140px;
        .content_text {
            max-width: 882px;
            margin: 0 auto;
            text-align: center;
            .text_tit {
                font-family: IBM Plex Mono;
                font-style: normal;
                font-weight: bold;
                font-size: 40px;
                color: #ffffff;
            }
            .text_info {
                font-family: PingFang SC;
                font-weight: normal;
                font-size: 20px;
                line-height: 30px;
                color: rgba(288, 288, 288, 0.8);
                margin-top: 20px;
            }
        }
    }
}
</style>
<style lang="scss" scoped>
@media screen and (max-width: 1500px) {
    .part8 {
        .text_info2 {
            top: 800px;
        }
    }
}
@media screen and (max-width: 1400px) {
    .part8 {
        .text_info2 {
            top: 780px;
        }
    }
}
@media screen and (max-width: 1300px) {
    .part8 {
        .text_info2 {
            top: 740px;
        }
    }
}
@media screen and (max-width: 1260px) {
    .part8 {
        .text_info2 {
            top: 740px;
        }
    }
}
@media screen and (max-width: 1220px) {
    .part8 {
        .text_info2 {
            top: 700px;
        }
    }
}
@media screen and (max-width: 1200px) {
    .part8 {
        .part8_imgs {
            .part8_img {
                padding-top: 80px;
            }
        }
        .text_info2 {
            top: 760px;
        }
    }
}
@media screen and (max-width: 1100px) {
    .part8 {
        .part8_imgs {
            .part8_img {
                padding-top: 80px;
            }
        }
        .text_info2 {
            top: 720px;
        }
    }
}
@media screen and (max-width: 1024px) {
    .part8 {
        .part8_content {
            padding: 0 10px;
            margin-top: 40px;
            .content_text {
                .text_tit {
                    font-size: 20px;
                }
                .text_info {
                    font-size: 16px;
                    margin-top: 18px;
                }
            }
        }
        .text_info2 {
            top: 680px;
            font-size: 20px;
        }
    }
}
@media screen and (max-width: 1000px) {
    .part8 {
        .text_info2 {
            top: 720px;
            font-size: 20px;
        }
    }
}
@media screen and (max-width: 960px) {
    .part8 {
        .text_info2 {
            top: 680px;
            font-size: 20px;
        }
    }
}
@media screen and (max-width: 900px) {
    .part8 {
        .part8_bj {
            .part8_imgs {
                .part8_bj {
                    height: 800px;
                }
                .part8_img {
                    padding-top: 20px;
                }
            }
        }
        .text_info2 {
            top: 620px;
            font-size: 20px;
        }
    }
}
@media screen and (max-width: 800px) {
    .part8 {
        .part8_imgs {
            .part8_img {
                padding-top: 40px;
            }
        }
        .text_info2 {
            top: 540px;
            font-size: 1.25rem;
        }
    }
}

@media screen and (max-width: 700px) {
    .part8 {
        .part8_imgs {
            .part8_img {
                padding-top: 80px;
            }
        }
        .text_info2 {
            top: 520px;
            font-size: 1.25rem;
        }
    }
}
@media screen and (max-width: 600px) {
    .part8 {
        .text_info2 {
            top: 450px;
            font-size: 1.25rem;
        }
    }
}
@media screen and (max-width: 500px) {
    .part8 {
        .text_info2 {
            top: 400px;
            font-size: 12px;
        }
    }
}
@media screen and (max-width: 400px) {
    .part8 {
        font-size: 40%;
        .part8_content {
            padding: 0 10px;
            margin-top: 20px;
            .content_text {
                .text_tit {
                    font-size: 18px;
                }
                .text_info {
                    font-size: 12px;
                    margin-top: 10px;
                    line-height: 16px;
                }
            }
        }
        .text_info2 {
            top: 520px;
            font-size: 1.25rem;
        }
    }
}
</style>