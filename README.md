<div align="center">

## A must have\!  Send HTML headers\.


</div>

### Description

This is the data that you must send to a server when requesting an HTML page. If you are useing a control such as the Microsoft Internet control then you do not need this. If you are builduing a source grabber or something liek that, then you will need this.
 
### More Info
 
at least some form of internet connection. I used mswinsck.ocx for my control and I have this code located in the winsock_connect event.

non so far


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[c0rrupt0](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/c0rrupt0.md)
**Level**          |Unknown
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, ASP \(Active Server Pages\) 
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/c0rrupt0-a-must-have-send-html-headers__1-3539/archive/master.zip)





### Source Code

```
'As you can see I have a winsock control named sckURL.
'You can change that to anythign you wish.
With sckURL
    .SendData "GET /" & tPage & " HTTP/1.1" & vbCrLf
    .SendData "Accept: text/plain" & vbCrLf
    .SendData "Accept-Language: en-us" & vbCrLf
    .SendData "Accept-Encoding: gzip, deflate" & vbCrLf
    .SendData "User-Agent: Mozilla/4.0 (compatible; MSIE 5.0; Windows 98; DigExt)" & vbCrLf
    .SendData "Host: " & varDom & vbCrLf
    .SendData "Connection: Keep-Alive" & vbCrLf & vbCrLf
  End With
```

