---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Second Parsons Practice page

## Parsons 3 (Line Based Grader)
Re-arrange the blocks below so they will work for Activity 3

If a block is incorrect, drag back into the left hand side stack
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "int lightLevel = 0;\n" +
    "int lux = 0;\n" +
    "void setup()\n" +
    "{\n" +
    "  Serial.begin(9600);\n" +
    "}\n" +
    "void loop()\n" +
    "{\n" +
    "  lightLevel = analogRead(A0);t\n" +
    "  lux = 10000 * pow(lightLevel, 2);\n" +
    "  Serial.print(&quot;Light level: &quot;);\n" +
    "  Serial.println(lightLevel);\n" +
    "  Serial.print(&quot;lux: &quot;);\n" +
    "  Serial.println(lux);\n" +
    "  delay(1000);\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
