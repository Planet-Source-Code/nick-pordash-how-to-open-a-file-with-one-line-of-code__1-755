<div align="center">

## How to open a file with one line of code\!


</div>

### Description

You create a funtion that can open a file with just one line of code.
 
### More Info
 
Form is your Form, RichTextBox is your RichTextBox, and

Commondialog is your Commondialog.

This code requires a Commondialog and a RichTextBox.

The file you just open in the richtextbox you picked.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Nick Pordash](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/nick-pordash.md)
**Level**          |Unknown
**User Rating**    |4.2 (161 globes from 38 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/nick-pordash-how-to-open-a-file-with-one-line-of-code__1-755/archive/master.zip)





### Source Code

```
Public Function Openf(frm As Form, Text As RichTextBox, Dialog As CommonDialog)
   On Error Resume Next
    Dialog.Filter = "Text Files (*.txt)|*.txt|All Files (*.*)|*.*|" 'Edit the filter how you want it
    Dialog.Flags = cdlOFNPathMustExist & cdlOFNHideReadOnly
    Dialog.Action = 1
    Screen.MousePointer = vbHourglass
    Text.Text = ""
    Text.LoadFile Dialog.filename
    frm.Show
    frm.Refresh
    Screen.MousePointer = vbNormal
End Function
Private Sub Command1_Click()
Call Openf(Me, RichTextBox1, CommonDialog1)
End Sub
```

