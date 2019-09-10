```
<script>
    if (window.location.href.indexOf('xxDevelopment') > -1) {
      (function () {
        var script = document.createElement("script");
        script.src = "https://cdn.bootcss.com/vConsole/3.3.0/vconsole.min.js";
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(script, s);
        script.onload = function () {
          try {
            new VConsole()
          } catch (error) {
          }
        }
      })();
    }
  </script>
  ```
  
  这段代码加在index底部。
  
  在地址栏输入?xxDevelopment关键字，可以在线上查错方面发挥作用。
