---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Second Parsons Practice page

## Parsons 2 (Line Based Grader)
Re-arrange the blocks below so they will work for Activity 2

If a block is incorrect, drag back into the left hand side stack

<div id="A1-sortableTrash" class="sortable-code"></div> 
<div id="A1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="A1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="A1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "int lightLevel = 0;\n" +
    "void setup()\n" +
    "{\n" +
    "  Serial.begin(9600);\n" +
    "}\n" +
    "void loop()\n" +
    "{\n" +
    "  lightLevel = analogRead(A0);\n" +
    "  Serial.print(&quot;Light level: &quot;);\n" +
    "  Serial.println(lightLevel);\n" +
    "  delay(1000);\n" +
    "}\n" +
    "  Serial.println(lightlevel); #distractor\n" +
    "  Serial.print(&quot;light level: &quot;); #distractor\n" +
    "  lightLevel = analogRead(A0) #distractor";
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
