<template>
    <div class="body">
        <div class="banner" :style="'background-image: url(\'' + bannerbgSvg + '\');width: 100%;background-size: cover;'">
            <div class="banner_bg"></div>
            <div class="banner_content max-width">
                <div class="banner_top">
                    <div class="flex_center">
                        <div class="banner_topTitle" title="4核 RTD1296 | DDR4 4GB | eMMC 5.0 8GB">
                            <img class="icon_left" :src="icon_left" />
                            <span>4核 RTD1296 | DDR4 4GB | eMMC 5.0 8GB</span>
                            <img class="icon_right" :src="icon_right" />
                        </div>
                    </div>

                    <div class="banner_topTit" title="EasePi ARS2">EasePi ARS2</div>
                    <div class="banner_topInfo" title="EasePi ARS2，是易有云团队推出的基于RTD1296处理器且带存储的软路由开发板">EasePi
                        ARS2，是易有云团队推出的基于RTD1296处理器且带存储的软路由开发板</div>
                    <div class="flex_center">
                        <a onclick="gtag('event', 'open_buy_link', {'method': 'Google'});"
                            href="https://item.taobao.com/item.htm?id=655381846734" class="banner_topBtn" title="立即抢购"
                            target="_blank">立即抢购</a>
                    </div>
                    <!-- <div class="flex_right">
                        <div class="banner_price">
                            <img :src="banner_pricetag" />
                        </div>
                    </div> -->
                </div>
                <div class="flex_center">
                    <div class="banner_bottom">
                        <img :src="pic_banner" :srcset="pic_banner + ', ' + pic_banner_2x + ' 2x'" alt />
                    </div>
                </div>
            </div>

            <div class="Side">
                <div class="cart">
                    <a onclick="gtag('event', 'open_buy_link', {'method': 'Google'});"
                        href="https://item.taobao.com/item.htm?id=655381846734" target="_black" class="shopping">
                        <img :src="icon_shopping" class="shoppning_img" />
                        <img :src="icon_shoppning_hover" class="shoppning_hover" />
                    </a>
                    <div class="service">
                        <img :src="icon_service" />
                        <div class="code">
                            <div class="code_center">
                                <p>扫码咨询淘宝客服</p>
                                <img :src="code" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import bannerSvg from "../public/svg/banner.svg"
import bannerbgSvg from "../public/svg/bannerbg.svg"
import icon_left from "../public/svg/icon_left.svg"
import icon_right from "../public/svg/icon_right.svg"
import banner_pricetag from "../public/svg/banner_pricetag.svg"
import pic_banner from "../public/home/pic_banner.png"
import pic_banner_2x from "../public/home/pic_banner_2x.png"
import icon_service from "../public/svg/icon_service.svg"
import icon_shopping from "../public/svg/icon_shopping.svg"
import code from "../public/home/code.png"
import icon_shoppning_hover from "../public/svg/icon_shoppning_hover.svg"
export default {
    data() {
        return {
            bannerSvg,
            bannerbgSvg,
            icon_left,
            icon_right,
            banner_pricetag,
            pic_banner,
            pic_banner_2x,
            icon_service,
            icon_shopping,
            code,
            icon_shoppning_hover
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

.body {
    background-color: #000;
    padding-bottom: 100px;

    .max-width {
        max-width: 1440px;
    }

    .banner {
        width: 100%;
        height: 810px;
        position: relative;

        .banner_bg {
            background-size: cover;
        }

        .banner_content {
            margin: 0 auto;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            flex-wrap: wrap;

            .flex_center {
                display: flex;
                width: 100%;
                justify-content: center;
                margin: 0;
            }

            .banner_top {
                flex: 0 0 100%;
                max-width: 942px;
                position: absolute;
                top: 168px;
                display: flex;
                justify-content: center;
                align-items: center;
                text-align: center;
                flex-wrap: wrap;

                .banner_topTitle {
                    font-size: 18px;
                    font-family: PingFangSC-Regular, PingFang SC;
                    font-weight: 400;
                    color: #ffd732;
                    line-height: 25px;
                    position: relative;
                    margin-top: -35px;

                    .icon_left {
                        position: absolute;
                        top: -10px;
                        left: -14px;
                    }

                    .icon_right {
                        position: absolute;
                        bottom: -6px;
                        right: -14px;
                    }
                }

                .banner_topTit {
                    font-size: 60px;
                    font-family: PingFangSC-Semibold, PingFang SC;
                    font-weight: 600;
                    color: #ffffff;
                    line-height: 84px;
                    padding-top: 6px;
                }

                .banner_topInfo {
                    font-size: 18px;
                    font-family: PingFangSC-Regular, PingFang SC;
                    font-weight: 400;
                    color: rgba(255, 255, 255, 0.63);
                    line-height: 28px;
                    margin-bottom: 40px;
                }

                .banner_topBtn {
                    width: 176px;
                    height: 66px;
                    background: #0060ff;
                    border-radius: 8px;
                    font-size: 24px;
                    font-family: PingFangSC-Semibold, PingFang SC;
                    font-weight: 600;
                    color: #ffffff;
                    line-height: 66px;
                }

                .banner_topBtn:hover {
                    opacity: 0.9;
                }

                .banner_price {
                    position: absolute;
                    right: 0;
                    bottom: -54px;
                }
            }

            .banner_bottom {
                position: absolute;
                top: 432px;

                img {
                    width: 474px;
                    max-width: 100%;
                }
            }
        }

        .Side {
            position: fixed;
            bottom: 20px;
            right: 0;
            z-index: 999;

            .cart {
                .shopping {
                    width: 64px;
                    height: 64px;
                    border-radius: 8px 0px 0px 8px;
                    background: #464646;
                    position: fixed;
                    bottom: 126px;
                    right: 0;
                    display: flex;
                    justify-content: center;
                    align-items: center;

                    .shoppning_hover {
                        display: none;
                    }
                }

                .service {
                    width: 64px;
                    height: 64px;
                    border-radius: 8px 0px 0px 8px;
                    background: #464646;
                    position: fixed;
                    bottom: 48px;
                    right: 0;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    cursor: pointer;

                    .code {
                        width: 180px;
                        height: 212px;
                        border-radius: 8px;
                        background: #464646;
                        position: fixed;
                        bottom: 46px;
                        right: 72px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        flex-wrap: wrap;
                        display: none;

                        .code_center {
                            text-align: center;
                            padding: 0 8px;

                            p {
                                color: #ffffff;
                                font-size: 16px;
                                line-height: 32px;
                                padding: 0;
                                margin: 0;
                                padding-bottom: 2px;
                                padding-top: 2px;
                            }

                            img {
                                width: 100%;
                            }
                        }
                    }
                }
            }

            .shopping:hover {
                background: #ffffff;
            }

            .shopping:hover .shoppning_hover {
                display: block;
            }

            .shopping:hover .shoppning_img {
                display: none;
            }

            .service:hover .code {
                display: block;
            }
        }
    }
}
</style>
<style lang="scss" scoped>
@media screen and (max-width: 1440px) {
    .body {
        .max-width {
            padding: 0 30px;
        }
    }
}

@media screen and (max-width: 1024px) {
    .body {
        .max-width {
            max-width: 920px;
            padding: 0 30px;
        }

        .banner {
            .banner_content {
                .banner_top {
                    max-width: 842px;

                    .banner_price {
                        img {
                            width: 180px;
                        }
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 719px) {
    .body {
        .max-width {
            max-width: 100%;
            padding: 0 10px;
        }

        .banner {
            .banner_content {
                display: block;

                .flex_right {
                    display: flex;
                    width: 100%;
                    justify-content: right;
                    margin: 0;
                }

                .banner_top {
                    z-index: 2;
                    padding: 0 10px;
                    position: relative;

                    .banner_topTitle {
                        font-size: 14px;
                        //margin: 0 66px;
                    }

                    .banner_topTit {
                        font-size: 46px;
                    }

                    .banner_topInfo {
                        font-size: 16px;
                    }

                    .banner_topBtn {
                        margin-top: -18px;
                        z-index: 4;
                        width: 140px;
                        height: 56px;
                        font-size: 18px;
                        line-height: 56px;
                    }

                    .banner_price {
                        position: relative;
                        top: 20px;
                        bottom: 0px;
                        margin-left: auto;

                        img {
                            max-width: 88%;
                        }
                    }
                }

                .banner_bottom {
                    position: relative;
                    top: 200px;
                    // margin-top: 100px;
                    max-width: 474px;
                    z-index: 1;

                    img {
                        width: 100%;
                        padding: 0 10px;
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 400px) {
    .body {
        padding-bottom: 0;

        .banner {
            height: 700px;
        }
    }
}
</style>
