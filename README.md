*This page contains all the resources that you need for Windows 10 and Microsoft Office*

[Office 365 ProPlus](http://officecdn.microsoft.com/db/492350F6-3A01-4F97-B9C0-C7C6DDF67D60/media/en-US/O365ProPlusRetail.img)

[Visio 2019](https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/media/en-us/VisioPro2019Retail.img)

[Windows 10 Media Creation Tool](https://go.microsoft.com/fwlink/?LinkId=691209)

[Office 2019](https://archive.org/download/OfficeProPlus2019Retail/OfficeProPlus2019Retail.iso)

__For the activation, copy the code given below & paste it in Command prompt (with admin rights, by running it as an administrator.)__


<code>Manual Activation for Office 365</code>
<pre>cd /d %ProgramFiles%\Microsoft Office\Office16 (for 64-bit version)
cd /d %ProgramFiles(x86)%\Microsoft Office\Office16 (for 32-bit version)</pre>

<pre>for /f %x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"</pre>

<code>KMS Activation for Office 365</code>
<pre>cd /d %ProgramFiles%\Microsoft Office\Office16 (for 64-bit version)
cd /d %ProgramFiles(x86)%\Microsoft Office\Office16 (for 32-bit version)</pre>
<pre> cscript ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99
cscript ospp.vbs /unpkey:BTDRB >nul
cscript ospp.vbs /unpkey:KHGM9 >nul
cscript ospp.vbs /unpkey:CPQVG >nul
cscript ospp.vbs /sethst:kms8.msguides.com
cscript ospp.vbs /setprt:1688
cscript ospp.vbs /act</pre>


<code>Batch Script for Office 365</code>
<pre>@echo off
title Activate Office 365 ProPlus for FREE - MSGuides.com&cls&echo ============================================================================&echo #Project: Activating Microsoft software products for FREE without software&echo ============================================================================&echo.&echo #Supported products: Office 365 ProPlus (x86-x64)&echo.&echo.&(if exist "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles%\Microsoft Office\Office16")&(if exist "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles(x86)%\Microsoft Office\Office16")&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_mak*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&echo.&echo ============================================================================&echo Activating your Office...&cscript //nologo slmgr.vbs /ckms >nul&cscript //nologo ospp.vbs /setprt:1688 >nul&cscript //nologo ospp.vbs /unpkey:WFG99 >nul&cscript //nologo ospp.vbs /unpkey:DRTFM >nul&cscript //nologo ospp.vbs /unpkey:BTDRB >nul&cscript //nologo ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99 >nul&set i=1
:server
if %i%==1 set KMS=kms7.MSGuides.com
if %i%==2 set KMS=kms8.MSGuides.com
if %i%==3 set KMS=kms9.MSGuides.com
if %i%==4 goto notsupported
cscript //nologo ospp.vbs /sethst:%KMS% >nul&echo ============================================================================&echo.&echo.
cscript //nologo ospp.vbs /act | find /i "successful" && (echo.&echo ============================================================================&echo.&echo #My official blog: MSGuides.com&echo.&echo #How it works: bit.ly/kms-server&echo.&echo #Please feel free to contact me at msguides.com@gmail.com if you have any questions or concerns.&echo.&echo #Please consider supporting this project: donate.msguides.com&echo #Your support is helping me keep my servers running everyday!&echo.&echo ============================================================================&choice /n /c YN /m "Would you like to visit my blog [Y,N]?" & if errorlevel 2 exit) || (echo The connection to my KMS server failed! Trying to connect to another one... & echo Please wait... & echo. & echo. & set /a i+=1 & goto server)
explorer "http://MSGuides.com"&goto halt
:notsupported
echo.&echo ============================================================================&echo Sorry! Your version is not supported.&echo Please try installing the latest version here: bit.ly/odt2k16
:halt
pause >nul</pre>

<code>Manual Activation for Visio 2019<code>
<pre>cd /d %ProgramFiles%\Microsoft Office\Office16</pre>
  If you are using 64 bit version of Visio 2019
<pre>cd /d %ProgramFiles(x86)%\Microsoft Office\Office16</pre>
  If you are using 32 bit version of Visio 2019
<pre>for /f %x in ('dir /b ..\root\Licenses16\visiopro2019vl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"</pre>
  
<code>KMS Activation for Visio 2019<code>
<pre>cscript ospp.vbs /inpkey:THE_CLIENT_KEY (Replace Client with KMS Key)
cscript ospp.vbs /sethst:kms8.msguides.com
cscript ospp.vbs /setprt:1688
cscript ospp.vbs /act</pre>
