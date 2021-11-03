---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 1

title: 
subtitle: 

design:
  columns: "1"
  background:
    image: sun.jpeg
    image_darken: 0
    image_parallax: false
    image_position: center
    image_size: cover
    text_color_light: true
  spacing:
    padding: ["20px", "0", "20px", "0"]
advanced:
  css_class: fullscreen
---
<style type="text/css">
    @keyframes scaleDraw {  /*定义关键帧、scaleDrew是需要绑定到选择器的关键帧名称*/
            0%{
                transform: scale(1);  /*开始为原始大小*/
            }
            25%{
                transform: scale(1.1); /*放大1.1倍*/
            }
            50%{
                transform: scale(1.2);
            }
            75%{
                transform: scale(1.3);
            }
        }
    .ballon{
            width: 150px;
            height: 200px;
            background: url("/pic/sun.jpeg");
            background-size: 150px 200px;
            -webkit-animation-name: scaleDraw; /*关键帧名称*/
            -webkit-animation-timing-function: ease-in-out; /*动画的速度曲线*/
            -webkit-animation-iteration-count: infinite;  /*动画播放的次数*/
            -webkit-animation-duration: 5s; /*动画所花费的时间*/
        }

</style>
<div>
  <img src="/pic/sun.jpeg", class='ballon'>
</div>