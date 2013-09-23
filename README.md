jsPatternLock
=============

An Andoid like pattern lock plugin using javascript and rapheal(a Javascript Library for SVG)


<a href="jsfiddle.net/ajai/TbuE6/" target="_blank">Click here for demo</a>

<h2>Documentation</h2>
<h4>How to use? </h4>
<b>Step 1:</b> Include the  following scripts in your head section (click here to download raphaeljs , click here to download pattern.js)
<br/>
<pre>
&lt;script src="raphael-min.js" type="text/javascript"&gt;&lt;/script&gt;
&lt;script src="pattern.js" type="text/javascript"&gt;&lt;/script&gt;
</pre>
<br/>
<b>Step 2:</b> Create an instance for the pattern with your custom properties and draw the pattern within the container with instance.draw(container).
</div>
<pre>
var s = new Pattern(properties);
s.draw(container);
</pre>
<br/><h4 style="text-align: left;">
Properties</h4>
<table>
    <tbody>
<tr style="background: #ddd;">
            <td valign="top" width="205"><b>Property
                </b></td>
            <td valign="top" width="205"><b>Description</b>
                </td>
            <td valign="top" width="205"><b>Default Value</b>
                </td>
        </tr>
<tr>
            <td valign="top" width="205">dimension
                </td>
            <td valign="top" width="205">Dimension of the patern
                <br>
<i>No. of rows</i>
                    x <i>No. of columns</i>
                <br>
Eg:
                <br>
dimension:‘5x5’
                </td>
            <td valign="top" width="205">3x3
                </td>
        </tr>
<tr>
            <td valign="top" width="205">patternRadius
                </td>
            <td valign="top" width="205">Radius of the pattern circle
                <br>
Eg:
                <br>
patternRadius:25
                </td>
            <td valign="top" width="205">20
                </td>
        </tr>
<tr>
            <td valign="top" width="205">patternGap
                </td>
            <td valign="top" width="205">Gap between each Pattern Circle
                <br>
Eg:
                <br>
patternGap:70
                </td>
            <td valign="top" width="205">50
                </td>
        </tr>
<tr>
            <td valign="top" width="205">outerColor
                </td>
            <td valign="top" width="205">Color of the Pattern Circle. The color value can be either hex color or hex gradient color
                <br>
Eg:<b> </b>
                <br>
outerColor:’#FC0000’
                <br>
outerColor :‘90-#239EE0:5-#1951A0:95’
                </td>
            <td valign="top" width="205">#333333
                </td>
        </tr>
<tr>
            <td valign="top" width="205">innerColor
                </td>
            <td valign="top" width="205">Color of the inner circle within the Pattern Circle
                <br>
Eg:
                <br>
innerColor:’#FC0000’
                <br>
innerColor :‘90-#239EE0:5-#1951A0:95’
                </td>
            <td valign="top" width="205">90-#239EE0:5-#1951A0:95
                </td>
        </tr>
<tr>
            <td valign="top" width="205">background
                </td>
            <td valign="top" width="205">Pattern box background color
                <br>
Eg:
                <br>
background:’#FF00F0’
                </td>
            <td valign="top" width="205">#000000
                </td>
        </tr>
<tr>
            <td valign="top" width="205">backgroundOpacity
                </td>
            <td valign="top" width="205">Pattern box background opacity
                <br>
Eg:
                <br>
background:0.5
                </td>
            <td valign="top" width="205">1
                </td>
        </tr>
<tr>
            <td valign="top" width="205">hoverColor
                </td>
            <td valign="top" width="205">Stroke color of Pattern Circle when mouse over
                <br>
Eg:
                <br>
hoverColor:’#FF00F0’
                </td>
            <td valign="top" width="205">#c8ee17
                </td>
        </tr>
<tr>
            <td valign="top" width="205">errorColor
                </td>
            <td valign="top" width="205">Stroke color of Pattern Circle for Invalid Pattern
                <br>
Eg:
                <br>
errorColor:’#FF00F0’
                </td>
            <td valign="top" width="205">#FF0000
                </td>
        </tr>
<tr>
            <td valign="top" width="205">padding
                </td>
            <td valign="top" width="205">Pattern Box padding
                <br>
Eg:
                <br>
padding:25
                </td>
            <td valign="top" width="205">Value of pattern radius
                </td>
        </tr>
<tr>
            <td valign="top" width="205">onFinish
                </td>
            <td valign="top" width="205">Handler to be executed when the user completes the pattern
                <br>
Eg:
                <br>
onFinish:function(value){
                <br>
}
                <br>
<i>value</i>
                    – value of the pattern drawn passed to the handler
                </td>
            <td valign="top" width="205">null
                </td>
        </tr>
</tbody>
</table>
<br>
<span style="font-size: large;"><span style="font-size: small;">also you can set the property values externally with the created pattern Object</span></span><br>
<h4 style="text-align: left;">
Functions</h4>
<table>
    <tbody>
<tr style="background: #ddd;">
            <td valign="top" width="163"><b>Function</b>
                </td>
            <td valign="top" width="311"><b>Description</b>
                </td>
            <td valign="top" width="130"><b>Return value</b>
                </td>
        </tr>
<tr>
            <td valign="top" width="163">draw (container)
                </td>
            <td valign="top" width="311">Draw the pattern within the container. Should be called with pattern instance.
                <br>
Eg:
                    <br>
<i>
                        s.draw(‘mydiv’);
                        <br>
                    </i>
                    Here ‘mydiv’ represents containerId
                <br>
s.draw(document.getElementById(‘mydiv’));
                </td>
            <td valign="top" width="130">Return Pattern Object
                </td>
        </tr>
<tr>
            <td valign="top" width="163">clear()
                </td>
            <td valign="top" width="311">Resets the pattern.
                <br>
Eg:
                    <br>
<i>s.clear();</i>
                </td>
            <td valign="top" width="130">Return Pattern Object
                </td>
        </tr>
<tr>
            <td valign="top" width="163">error()
                </td>
            <td valign="top" width="311">Used to mark the drawn pattern as error
                <br>
Eg:
                    <br>
<i>s.error();</i>
                </td>
            <td valign="top" width="130">Return Pattern Object
                </td>
        </tr>
<tr>
            <td valign="top" width="163">val()
                </td>
            <td valign="top" width="311">Used to get the value of drawn pattern
                <br>
Eg:
                    <br>
<i>s.val();</i>
                    <br>
for the image attached in this post, the value returned will be ‘<i>3-4-5-10-15</i><i>’</i>
                </td>
            <td valign="top" width="130">Return pattern value
                </td>
        </tr>
</tbody>
</table>
