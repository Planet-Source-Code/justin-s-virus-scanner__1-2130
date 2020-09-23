<div align="center">

## Virus Scanner


</div>

### Description

This is kind of a Virus Scanner...It's to let you get the feel

of a scanner which searches for strings a virus might have and

then displays that it is a virus in a message box. Put this in

a module and call it from like a button or something. I am only

13 so if you think this code is dumb or wouldn't work...sorry

im still learning. E-Mail me at BmFWaLk316@Juno.com if you have

any problems. Later.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Justin S\.](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/justin-s.md)
**Level**          |Unknown
**User Rating**    |4.0 (20 globes from 5 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__1-5.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/justin-s-virus-scanner__1-2130/archive/master.zip)





### Source Code

```
Function Scanner(File As String)
Infected = 0
Trojan = 0
Dim BO As Integer
Dim FileLenn As Variant
Dim FileLennn As Variant
Dim l003A As Variant
Dim l003E As Variant
Dim l0039 As String
Dim l0001 As Single
Dim l0002 As Single
Dim l0003 As Single
Dim l0004 As Single
Dim l0005 As Single
Dim l0006 As Single
Dim l0007 As Single
Dim l0008 As Single
Dim l0009 As Single
Dim l0010 As Single
Dim l0011 As Single
Dim l0012 As Single
Dim l0013 As Single
Dim l0014 As Single
Dim l00530 As Single
If LCase(Right$(File, 3)) = "swp" Then MsgBox "File Is a System.swp File": Exit Function
Open File For Binary As #2
DoEvents
FileLenn = LOF(2)
FileLennn = FileLenn
l003A = 1
While FileLennn >= 0
  If FileLennn > 32000 Then
   l003E = 32000
  ElseIf FileLennn = 0 Then
   l003E = 1
  Else
   l003E = FileLennn
  End If
   l0039$ = String$(l003E, " ")
 Get #2, l003A, l0039$
  l0001! = InStr(1, l0039$, "@juno.com", 1)
  l0002! = InStr(1, l0039$, "@hotmail.com", 1)
  l0003! = InStr(1, l0039$, "@rocketmail.com", 1)
  l0004! = InStr(1, l0039$, "Password", 1)
  l0005! = InStr(1, l0039$, "Screen Name", 1)
  l0006! = InStr(1, l0039$, "win32.exe", 1)
  l0007! = InStr(1, l0039$, "STEALER1", 1)
  l0008! = InStr(1, l0039$, "PWSTEAL", 1)
  l0009! = InStr(1, l0039$, "usa.com", 1)
  l0010! = InStr(1, l0039$, "Remove Directory", 1)
  l0011! = InStr(1, l0039$, "autoapp", 1)
  l0012! = InStr(1, l0039$, "deltree /y", 1)
  l0013! = InStr(1, l0039$, "kill *.*", 1)
  l0014! = InStr(1, l0039$, "load", 1)
  l00530! = InStr(1, l0039$, "win.ini", 1)
If l0001! Then Infected = 1: MsgBox "File Sends Mail To juno.com": Exit Function
If l0002! Then Infected = 1: MsgBox "File Sends Mail To hotmail.com": Exit Function
If l0003! Then Infected = 1: MsgBox "File Sends Mail To rocketmail.com": Exit Function
If l0004! Then Infected = 1: MsgBox "File Contains The String 'Password'": Exit Function
If l0005! Then Infected = 1: MsgBox "File Contains The String 'Screen Name'": Exit Function
If l0006! Then Infected = 1: MsgBox "File Loads Itself As 'Win32'": Exit Function
If l0007! Then Infected = 1: MsgBox "File Is An AOL Trojan": Exit Function
If l0008! Then Infected = 1: MsgBox "File Is An AOL Trojan": Exit Function
If l0009! Then Infected = 1: MsgBox "File Sends Mail To usa.com": Exit Function
If l0010! Then Infected = 1: MsgBox "File Removes Directories": Exit Function
If l0011! Then Infected = 1: MsgBox "File Is Probably An Auto Mailer": Exit Function
If l0012! Then Infected = 1: MsgBox "File Is A Deltree": Exit Function
If l0013! Then Infected = 1: MsgBox "File Is A Virus": Exit Function
If l0014! And l00530! Then Infected = 1: MsgBox "File Writes To The 'win.ini' File ": Exit Function
If BO = 3 And FileLenn = 124928 Then Trojan = 1: MsgBox "File Is The BackOrifice.Trojan": Exit Function
If Not l0001! Or Not 10002! Or Not 10003 Or Not 10004! Or Not 10005! Or Not 10006! Or Not l0007! Or Not l0008! Or Not l0009! Or Not l0010! Or Not l0011! Or Not l0012! Or Not l0013! Or Not l0014! Then Infected = 0: MsgBox "No Virus Found": Exit Function
Wend
End Function
```

