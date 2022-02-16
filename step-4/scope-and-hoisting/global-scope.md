# Global Scope

앞서 소개해드렸던 Global Scope는 일반적으로 신중하여 생각해보고 사용해야 합니다. 아래의 예제 코드를 한번 실행해보세요.

{% tabs %}
{% tab title="XML/HTML/SVG" %}
{% code title="Global Scope Example" %}
```markup
<html>
  <head>
    <title>Global Scope Sample</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <script>
      var a = '바닐라코딩';

      console.log(`우리는 ${a}입니다.`);

      setTimeout(function () {
        console.log(`[1초 후] 우리는 ${a}입니다.`);
      }, 1000);
    </script>
    <script>
      var a = '느린캠퍼스';

      console.log(`우리는 ${a}입니다.`);
    </script>
  </body>
</html>
```
{% endcode %}

위 예제를 실행했을때 콘솔에 어떤 결과가 출력되었나요? 그 이유에 대해서 잘 생각해보시기 바랍니다.
{% endtab %}
{% endtabs %}

위 예제에서 보셨듯이, 하나의 HTML 페이지에는 출처가 다른 여러 개의 script가 들어갈 수 있습니다. 그리고 Global Scope를 자유롭게 사용한 결과, 위와 같이 코드 출력 결과가 나왔습니다.

쉽게 말씀드리자면, Global Scope란 공용공간이라고 보시면 좋을것 같습니다.

여러분은 공용공간을 사용하실때 어떻게 사용하시나요? 만약 여러분이 아끼는 맥북 프로를 신도림역 1번 출구에 1시간 동안 가져다 놓고 근처 스타벅스에 다녀온다고 생각해보세요. 맥북 프로가 어떻게 될 것이라고 예상하시나요?

**하나의 웹 페이지에는 하나의 Global Scope가 존재하고, 그 곳은 여러 개의 script가 사용할 수 있는 공용공간입니다. 우리가 어떤 물건을 공용공간(Global Scope)에 배치해둔다면, 다른 누군가가 그 물건을 사용할 수도 있고 혹은 수정/삭제할 가능성도 있습니다.**

**물론 절대 사용하면 안된다는 의미는 아닙니다.** 필요하다면 반드시 사용해야 하지만, 주의를 기울여 신중하게 사용해야만 합니다.
