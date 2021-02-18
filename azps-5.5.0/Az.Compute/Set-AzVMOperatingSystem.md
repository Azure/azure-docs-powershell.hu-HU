---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204711"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Beállítja az operációs rendszer tulajdonságait egy virtuális géphez.

## SZINTAXIS

### Windows (alapértelmezett)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMOperatingSystem** parancsmag beállítja egy virtuális gép operációs rendszerének tulajdonságait.
Megadhatja a bejelentkezési hitelesítő adatokat, a számítógép nevét és az operációs rendszer típusát.

## PÉLDÁK

### 1. példa: Az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Az első parancs biztonságos karakterláncra konvertálja a jelszót, majd tárolja azt a $SecurePassword változóban.
További információért írja be a `Get-Help ConvertTo-SecureString` .
A második parancs létrehoz egy hitelesítő adatokat a felhasználó FullerP-hez és a $SecurePassword-ban tárolt jelszóhoz, majd a hitelesítő adatokat a $Credential változóban tárolja.
További információért írja be a `Get-Help New-Object` .
A harmadik parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet változóban tárolja.
A negyedik parancs létrehoz egy virtuális gépobjektumot, majd tárolja azt a $VirtualMachine változóban.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.
A következő négy parancs értékeket rendel a változókhoz, amelyek az alábbi parancsban használhatók.
Mivel ezeket a karakterláncokat közvetlenül a **Set-AzVMOperatingSystem** parancsban is megadhatja, ezt a módszert csak az olvashatóság érdekében használjuk.
A parancsfájlok azonban ehhez hasonló módszert is használhatnak.
Az utolsó parancs beállítja az operációs rendszer tulajdonságait a $VirtualMachine.
A parancs a $Credential.
A parancs bizonyos paraméterekhez a korábbi parancsokban hozzárendelt változókat használja.

## PARAMETERS

### -ComputerName
A számítógép nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hitelesítő adatok
A virtuális gép felhasználónevét és jelszavát adja meg **PSCredential objektumként.**
Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot.
További információért írja be a `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Egy 64-es alapkódolt egyéni adatokat kódolt karakterláncot ad meg.
Ezt egy bináris tömbbe dekódolja a rendszer, amely fájlként van mentve a virtuális gépre.
A bináris tömb maximális hossza 65535 bájt.<br>
**Megjegyzés: Az egyéniData tulajdonságban ne adja át a titkosságokat és jelszavakat**<br>
A virtuális gép létrehozása után ez a tulajdonság nem frissíthető. <br>
A customData át van jelölve a VM-nek fájlként való [mentéshez,](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) további információt az Azure virtuális gépeken található Egyéni adatok <br>
Ha felhőbeli initet használ LinuxOS VM-hez, tekintse meg [a Linux VM testreszabása felhőbeli init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) használatával a készítés során

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Tiltsa le a Virtuális gép kiépítési ügynökének funkcióját.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Azt jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Azt jelzi, hogy az operációs rendszer típusa Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
A vendégen keresztüli javítás módja az IaaS virtuális gépre.<br><br>
Lehetséges értékek:<br>
**Kézi** – Ön szabályozhatja a javítások virtuális gépre való alkalmazását. Ehhez manuálisan kell telepítenie a javításokat a VM-en belül. Ebben a módban az automatikus frissítések le vannak tiltva; A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak hamisnak kell lennie<br>
**AutomaticByOS** – A virtuális gépet automatikusan frissíti az operációs rendszer. A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak igaznak kell lennie. <br >
**AutomaticByPlatform** – a virtuális gép automatikusan frissül az operációs rendszer által. A provisionVMAgent és a WindowsConfiguration.enableAutomaticUpdates tulajdonságnak teljesülnie kell

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Azt jelzi, hogy a beállításokhoz telepíteni kell a virtuális gép ügynökét a virtuális gépre.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
A virtuális gép időzónáját határozza meg. például a \" csendes-óceáni téli \" idő. <br>
A lehetséges értékek a [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [által visszaadott](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) időzónákból származó TimeZoneInfo.Id is beállíthatók.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a helyi virtuális gépobjektumot adja meg, amelyen meg kell állítani az operációs rendszer tulajdonságait.
Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.
Virtuális gépi objektum létrehozása a New-AzVMConfig parancsmag használatával.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
Azt jelzi, hogy az operációs rendszer típusa Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Egy WinRM-tanúsítvány URI-ját adja meg.
Ezt egy kulcstárolóban kell tárolni.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Azt jelzi, hogy az operációs rendszer HTTP WinRM-et használ.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Azt jelzi, hogy ez az operációs rendszer HTTPS WinRM-et használ.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


