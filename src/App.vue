<template>
  <div id="app">
    <app-header></app-header>
    <sidebar></sidebar>
    <app-content></app-content>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from '@/layout/AppHeader'
import Sidebar from '@/layout/Sidebar'
import AppContent from '@/layout/AppContent'
import AppFooter from '@/layout/AppFooter'
export default {
  name: 'app',
  components: {
    AppHeader,
    Sidebar,
    AppContent,
    AppFooter
  }
}
</script>

<style lang="scss">
  /* HTML Reset */
  body{background-color:#fff;}
  body,table,input,select,textarea,button{font-family:verdana, '나눔고딕', '맑은 고딕', sans-serif;font-size:12px;color:#333;}
  header,footer,section,article,aside,nav,hgroup,details,menu,figure,figcaption{display: block}
  button,input[type=submit],input[type=reset],input[type=button]{cursor:pointer;overflow:visible}
  body{margin:0;/*word-wrap:break-word*/}
  hr{display:none}
  .commentform input,
  .commentform textarea,
  #tpg-commentform textarea{border:1px solid #CCC;padding:.1em}
  input.etc,
  textarea.etc{border:0}
  img{border:0}
  label{cursor:pointer}
  acronym,
  abbr{cursor:help}
  a{text-decoration:none;color:#333;}

  p,ul,ol,dl,h1,dd,li{margin:0;padding:0;list-style:none; }

  .clfix:after {content: "."; display: block; height: 0px; clear: both; visibility: hidden;}
  .clfix {display: inline-block;}
  .clfix {display: block;}
  * html .clfix {height: 1%;} /* Hides from IE-mac */
  .clfix { zoom:1; } /*for IE 5.5-7*/
  .cl-le {clear:left;}

  /* All Device (모든 해상도를 위한 공통 코드를 작성한다. 모든 해상도에서 이 코드가 실행됨) */
  #app {}
  header {clear:both; display:block; border-bottom:4px solid blue; margin:0 0 1em; padding:2em 0 0; }
  header ul.desc {padding:0 0 1em 1em; color:#999; }
  header ul.desc a {color:#999; text-decoration:underline; }

  section {}

  section article {}
  section article h1 {}
  section article .projectDetail {position:relative; }
  section article dl {background:url("./assets/bg_hline01.gif") repeat-x left bottom; padding:1em; }
  section article dl.last {background:none; }
  section article dl:after {content: "."; display: block; height: 0px; clear: both; visibility: hidden;}
  section article dl {display: inline-block;}
  section article dl {display: block;}
  section article dl dt {}
  section article dl dd.btnTop {position:absolute; right:10px; top:15px; }
  section article dl dd.btnTop a {display:inline-block; *zoom:1; *display:block; width:30px; height:14px; line-height:12px; text-align:center; color:#ccc; border:1px solid #ddd; border-radius:5px; }
  section article dl dd ul {padding:0.5em 1em; }
  section article dl dd ul li {padding-left:2em; background:url("./assets/bul_point.gif") no-repeat left 50%; }

  /* Mobile Device (768px 미만 해상도의 모바일 기기를 위한 코드를 작성한다. 모든 해상도에서 이 코드가 실행됨. 미디어 쿼리를 지원하지 않는 모바일 기기를 위해 미디어 쿼리 구문을 사용하지 않는다) */
  #app {width:auto; margin:0 1em; }
  section {float:none; width:auto;}
  section article dl {width:auto; padding:1em 0.5em; }
  section article dl dt {font-weight:bold; font-size:14px; padding:0 0 0.5em 0; }
  section article dl dd.siteThum {float:none; width:auto; }
  section article dl dd.siteThum img {width:100%; }
  nav {position:relative; left:0; top:0; width:100%; font-size:11px; text-align:left; margin:0; }
  nav dl dt {padding:1em 2px 4px; border-bottom:1px solid #ddd; }
  nav ul {}
  nav ul li {float:left; width:50%; background:url("./assets/bg_hline01.gif") repeat-x left bottom; }
  nav ul li a {display:block; padding:5px 0 5px 2em; background:url("./assets/bul_folder.gif") no-repeat left 50%; }

  /* Tablet & Desktop Device (사용자 해상도가 768px 이상일 때 이 코드가 실행됨. 테블릿과 데스크톱의 공통 코드를 작성한다) */
  @media all and (min-width:768px) {

    nav {position:fixed; left:50%; top:100px; width:150px; letter-spacing:-0.02em; margin-left:215px; }
    nav ul li {float:none; width:auto;}
    section article dl dd.btnTop {display:none; }
    section article dl dd {float:left; }
    section article dl dd.siteThum {float:left; width:200px; }

    section {width:570px; }

    footer {clear:both; border-top:2px solid #ddd; padding:1em 0 2em; }
    footer .desc {font-size:11px; color:#555; }
  }

  /* Tablet Device (사용자 해상도가 768px 이상이고 1023px 이하일 때 이 코드가 실행됨. 아이패드 또는 비교적 작은 해상도의 랩탑이나 데스크톱에 대응하는 코드를 작성한다) */
  @media all and (min-width:768px) and (max-width:1023px) {
    #app{margin:0 1em; }
  }

  /* Desktop Device (사용자 해상도가 1024px 이상일 때 이 코드가 실행됨. 1024px 이상의 랩탑 또는 데스크톱에 대응하는 코드를 작성한다) */
  @media all and (min-width:1024px) {
    #app {width:980px; margin:0 auto; }
    section {width:720px; }
    nav {position:fixed; left:50%; top:100px; width:200px; letter-spacing:-0.02em; margin-left:280px; overflow-y: scroll; }
  }

</style>
