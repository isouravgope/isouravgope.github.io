```
Sub Formatings()
'
' Formatings Macro
' To add Bold, Italic, Underline
'Application.ScreenUpdating = False

With ActiveDocument.Range
Dim colindx
colindx = 0

  With .Find

    .ClearFormatting

    .Replacement.ClearFormatting

    '.Font.ColorIndex = wdAutomatic
    
    .Forward = True

    .Wrap = wdFindContinue

    .Format = True

    .Text = ""
    
    .Font.Bold = True
    .Replacement.Text = "<b>^&</b>"


    .Execute Replace:=wdReplaceAll

    .ClearFormatting

    .Font.Italic = True

    .Replacement.Text = "<i>^&</i>"

    .Execute Replace:=wdReplaceAll

    .ClearFormatting

    .Font.Underline = True

    .Replacement.Text = "<u>^&</u>"

    .Execute Replace:=wdReplaceAll

  End With

End With
Debug.Print (colindx)
Application.ScreenUpdating = True
 
End Sub



```
