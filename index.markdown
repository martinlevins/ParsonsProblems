---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Parson's Problems
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
## Re-arrange the blocks below so they print out "Hello World!"

<div id="p1-sortableTrash" class="sortable-code"></div>
<div id="p1-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p1-feedbackLink" value="Get Feedback" type="button" />
    <input id="p1-newInstanceLink" value="Reset Problem" type="button" />
</p>

[comment]: # Change below Generator is at : https://codio.github.io/parsons-puzzle-ui/dist/

<div id="Activity 1-sortableTrash" class="sortable-code"></div> 
<div id="Activity 1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Activity 1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Activity 1-newInstanceLink" value="Reset Problem" type="button" /> 
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
    "while (false) #distractor\n" +
    "void set up () #distractor\n" +
    "  Serial.begin(9600) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Activity 1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "Activity 1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Activity 1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Activity 1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


