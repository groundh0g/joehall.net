---
layout: default
---

<br/>
<div class="row">
  <div class="col-md-6"><img class="home-img" src='{{ "assets/images/joe.png" | relative_path }}'/></div>
  <div class="col-md-6" class="home-text">
    <div class="home-greet" id="divGreeting" title="Hello!">hello</div>
    <div class="home-moniker">I'm Joseph Hall.</div>
    <div class="home-moniker">a.k.a. <span style="font-family: 'Source Code Pro', monospace;">groundh0g</span></div>
    <div class="home-bio">&nbsp;</div>
    <div class="home-bio">Programmer. Writer. Artist. Teacher.</div>
    <div class="home-bio">Juggler. Musician. Punster. Dad. Husband.</div>
    <div class="home-bio">Thoughtworker. ex-IBMer. ex-Microsoftie.</div>
    <div class="home-bio">
        <br/>
        <br/>
    </div>
  </div>
</div>

<script type="text/javascript">
var greetings = ['hello', 'howdy', 'greetz', '你好', 'aloha', 'hallå', 'नमस्ते', 'hallo', 'olá', '여보세요', 'buna', 'שלום', 'bonjour', 'مرحبا', 'cześć', 'Բարեւ', 'unjani', 'как дела', 'ਤੁਸੀ ਕਿਵੇਂ ਹੋ', 'salve', 'ciao', 'sawubona'];
var iHello = -1;

var getText = function() {
    iHello = (iHello + 1) % greetings.length;
    $("#divGreeting").text(greetings[iHello]);
    setTimeout(getText, (greetings[iHello] === 'hello' ? 4000 : 1000));
};

getText();

</script>