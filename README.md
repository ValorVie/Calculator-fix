## Reset
The name might be "Calculator" or "小算盤".
![[pic/1.png]]

![[pic/2.png]]
If this does not solve the problem.

## Reinstall
```
git clone https://github.com/ValorVie/Calculator-fix.git

# Remove
Get-AppxPackage *windowscalculator* | Remove-AppxPackage

# Open CMD with system privileges.
cd Calculator-fix\PSTools
psexec -s -i cmd.exe

# Remove residual data.
cd "C:\Program Files\WindowsApps"
mkdir _bak
move Microsoft.WindowsCalculator_10_... _bak
move Microsoft.WindowsCalculator_10_... _bak
move Microsoft.WindowsCalculator_10_... _bak
move Microsoft.WindowsCalculator_2020_... _bak

move Microsoft.WindowsCalculator_10.2103.8.0_neutral_split.language-zh-hant_8wekyb3d8bbwe _bak
move Microsoft.WindowsCalculator_10.2103.8.0_neutral_split.scale-100_8wekyb3d8bbwe _bak
move Microsoft.WindowsCalculator_10.2103.8.0_x64__8wekyb3d8bbwe _bak
move Microsoft.WindowsCalculator_2020.2103.8.0_neutral_~_8wekyb3d8bbwe _bak

# Install Calculator
Add-AppPackage -Path "C:\Users\user\Desktop\Calculator-fix\Microsoft.WindowsCalculator_2020.2103.8.0_neutral_~_8wekyb3d8bbwe.AppxBundle"

Or use the mouse to click the AppxBundle File to proceed with the installation.
```

# Reference
[Steps to Fix Windows 10 Calculator is Missing Error](https://wethegeek.com/steps-to-fix-windows-10-calculator-is-missing-error/)  
[How to install Microsoft Calculator on a Windows 10 Pro 20H2 device that doesn't have access to Internet? - Microsoft Q&A](https://learn.microsoft.com/en-us/answers/questions/428962/how-to-install-microsoft-calculator-on-a-windows-1)  
[Microsoft Store - Generation Project (v1.2.3) [by @rgadguard & mkuba50]](https://store.rg-adguard.net/)  
[Fixing Microsoft Store error 0x80073cf9 when trying to install or update a specific app – codeinsecurity](https://codeinsecurity.wordpress.com/2021/12/01/fixing-microsoft-store-error-0x80073cf9-when-trying-to-install-or-update-a-specific-app/)  
[How to Install .Appx or .AppxBundle Software on Windows 10](https://www.howtogeek.com/285410/how-to-install-appx-or-appxbundle-software-on-windows-10/)  