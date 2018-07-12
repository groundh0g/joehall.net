---
layout: default
---

<br/>
<div class="row">
  <div class="col-md-6"><img style="width:100%" src='{{ "assets/images/joe.png" | relative_path }}'/></div>
  <div class="col-md-6" style="text-align: center">
    <br/><br/>
    <div style="font-size: 5.0em" id="divGreeting" title="Hello!">hello</div>
    <div style="font-size: 2.0em">I'm Joseph Hall.</div>
    <div style="font-size: 2.0em">a.k.a. <span style="font-family: 'Source Code Pro', monospace;">groundh0g</span></div>
    <div style="font-size: 1.0em">&nbsp;</div>
    <div style="font-size: 1.0em">Programmer. Writer. Artist. Teacher.</div>
    <div style="font-size: 1.0em">Juggler. Musician. Punster. Dad. Husband.</div>
    <div style="font-size: 1.0em">ex-ThoughtWorks. ex-IBM. ex-Microsoft.</div>
    <br/><br/>
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