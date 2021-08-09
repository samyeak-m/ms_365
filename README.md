# ms_365
Activation_cmd_code
Steps:

1.  Download and install Office 365
2.  Remove current trial license
3.  Open command prompt as admin
4.  Navigate to the Office folder
     cd /d %ProgramFiles%\Microsoft Office\Office16
     cd /d %ProgramFiles(x86)%\Microsoft Office\Office16
5.  Convert your Office license to volume one if possible
     for /f %x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"
6.  Use KMS client key to activate your Office
      cscript ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99
      cscript ospp.vbs /unpkey:BTDRB >nul
      cscript ospp.vbs /unpkey:KHGM9 >nul
      cscript ospp.vbs /unpkey:CPQVG >nul
      cscript ospp.vbs /sethst:kms8.msguides.com
      cscript ospp.vbs /setprt:1688
      cscript ospp.vbs /act
