# jade-email-doc

Create email bodies with backgrounds.

[Read more](http://backgrounds.cm/).

## How it works

Write email code in Jade, using `+body` for the mixin:

```jade
include ../email-body.jade

+body(bgcolor = '#FF0', background = "image.ext")
```

And get a much more intense output, voila!

```html
<div style="background-color:#FF0;">
  <!-- [if gte mso 9]
  <v:background xmlns:v="urn:schemas-microsoft-com:vml" fill="t">
    <v:fill type="tile" src="image.ext" color="#FF0"></v:fill>
  </v:background>
  -->
  <table height="100%" width="100%" cellpadding="0" cellspacing="0" border="0">
    <tr>
      <td valign="top" align="left" background="image.ext">
      </td>
    </tr>
  </table>
</div>
```