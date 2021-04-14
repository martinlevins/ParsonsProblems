---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons Question 1
Some directions as to what the student is re-arranging the code to do.....

<div id="p1-sortableTrash" class="sortable-code"></div>
<div id="p1-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p1-feedbackLink" value="Get Feedback" type="button" />
    <input id="p1-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript"> (function(){ var initial = "void setup ()\n" + "{\n" + " Serial.begin(9600);\n" + "}\n" + "void loop()\n" + "{\n" + "while (true)\n" + " {\n" + " Serial.println("test");\n" + " delay(1000);\n" + " }\n" + "}"; var parsonsPuzzle = new ParsonsWidget({ "sortableId": "sortable", "max_wrong_lines": 10, "grader": ParsonsWidget._graders.LineBasedGrader, "exec_limit": 2500, "can_indent": true, "x_indent": 50, "lang": "en" }); parsonsPuzzle.init(initial); parsonsPuzzle.shuffleLines(); $("#newInstanceLink").click(function(event){ event.preventDefault(); parsonsPuzzle.shuffleLines(); }); $("#feedbackLink").click(function(event){ event.preventDefault(); parsonsPuzzle.getFeedback(); }); })(); </script>


