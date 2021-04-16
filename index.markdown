---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they will work for Activity 1 ACARA

<div id="A1-sortableTrash" class="sortable-code"></div> 
<div id="A1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="A1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="A1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "void setup ()\n" +
    "{\n" +
    "  Serial.begin(9600);\n" +
    "}\n" +
    "void loop()\n" +
    "{\n" +
    "while (true)\n" +
    "  {\n" +
    "  Serial.println(&quot;test&quot;);\n" +
    "  delay(1000);\n" +
    "  }\n" +
    "}\n" +
    "While (True) #distractor\n" +
    "  Serial.println(&quot;test&quot;) #distractor\n" +
    "  Serial.Begin(9600); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "A1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "A1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#A1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#A1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
