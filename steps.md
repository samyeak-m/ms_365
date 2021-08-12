# ms_365
Activation_cmd_code
1.   Steps:

1.  Download and install Office 365
2.  Remove current trial license
3.  Open command prompt as admin
4.  Navigate to the Office folder
    1.    cd /d %ProgramFiles%\Microsoft Office\Office16
    2.    cd /d %ProgramFiles(x86)%\Microsoft Office\Office16
5.  Convert your Office license to volume one if possible
    1.    for /f %x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"
    2.    cscript ospp.vbs /inslic:"..\root\Licenses16\ProPlusVL_KMS_Client-ul-oob.xrm-ms"
    3.    cscript ospp.vbs /inslic:"..\root\Licenses16\ProPlusVL_KMS_Client-ul.xrm-ms"
6.  Use KMS client key to activate your Office
     1.   cscript ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99
     2.   cscript ospp.vbs /unpkey:BTDRB >nul
     3.   cscript ospp.vbs /unpkey:KHGM9 >nul
     4.   cscript ospp.vbs /unpkey:CPQVG >nul
     5.   cscript ospp.vbs /sethst:kms8.msguides.com
     6.   cscript ospp.vbs /setprt:1688
     7.   cscript ospp.vbs /act
