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


---
<style type="text/css">
    @keyframes scaleDraw {  /*定义关键帧、scaleDrew是需要绑定到选择器的关键帧名称*/
            0%{
                transform: scale(1.3);  /*开始为原始大小*/
            }
            100%{
                transform: scale(1);
            }
        }
    .ballon{

            background-image: url('/pic/sun.jpeg');
            width: 100%;
            height: 100%;
            max-width: 100%;
            max-height: 100%;
            background-size: cover;
            -moz-background-size: 100% 100%;

            -webkit-animation-name: scaleDraw; /*关键帧名称*/
            -webkit-animation-timing-function: ease-in-out; /*动画的速度曲线*/
            -webkit-animation-iteration-count: 1;  /*动画播放的次数*/
            -webkit-animation-duration: 15s; /*动画所花费的时间*/
        }
    @keyframes fadeIn {
      0% { 
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
    .fade {
      -webkit-animation: fadeIn 2s 2s 1;
      animation: fadeIn 2s 2s 1; 
    }
    #welcome_str{
      font-family: arial,"Hiragino Sans GB","Microsoft Yahei",sans-serif;
      font-size:3.5em;
      color: black;

    }
</style>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
<script type="text/javascript">
  $(document).ready(function (){
    $('#image').append("<img class='ballon' src='/pic/sun.jpeg' id='bg_img'><span id='welcome_str' class='fade' style='position: absolute; top: 0; left: 0;'>WELCOME TO SRI'S LAB</span>");
    console.log('bg_img.width='+$('#bg_img').width());
    console.log('window width='+$(window).width());
    $('#image').css('padding', 0);
    $('#bg_img').css('height', $(window).height() - $('#navbar-main').height());
    $('#welcome_str').css('left',($(window).width() - $('#welcome_str').width())/2);
    $('#welcome_str').css('top',($(window).height() - $('#navbar-main').height())/2 - 50);

  })
</script>
