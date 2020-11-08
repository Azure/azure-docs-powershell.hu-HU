---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187493"
---
# Set-AzVMOperatingSystem

## Áttekintés
A virtuális gépek operációs rendszerének tulajdonságait állítja be.

## SZINTAXISA

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

## Leírás
A **set-AzVMOperatingSystem** parancsmag a virtuális gépek operációs rendszerének tulajdonságait állítja be.
Megadhatja a bejelentkezési hitelesítő adatait, a számítógép nevét és az operációs rendszer típusát.

## Példák

### 1. példa: az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez
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

Az első parancs a jelszót egy biztonságos karakterláncba konvertálja, majd a $SecurePassword változóban tárolja.
További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .
A második parancs létrehozza a hitelesítő adatokat a felhasználói FullerP és a $SecurePassword tárolt jelszóhoz, majd a $Credential változóban tárolja a hitelesítő adatokat.
További információért írja be a következőt: `Get-Help New-Object` .
A harmadik parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.
A negyedik parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.
A következő négy parancs az alábbi parancsban használható változók értékeit társítja.
Mivel ezeket a karakterláncokat közvetlenül megadhatja a **set-AzVMOperatingSystem** parancsban, ez a megközelítés csak az olvashatóság érdekében használatos.
Használhatja azonban a parancsfájlokban például ezt a módszert.
A végleges parancs beállítja az operációs rendszer tulajdonságait az $VirtualMachine tárolt virtuális gépnek.
A parancs a $Credentialban tárolt hitelesítő adatokat használja.
A parancs bizonyos paraméterek esetében az előző parancsokban megadott változókat használja.

## PARAMÉTEREK

### -Számítógépnév
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
A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.
Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.
További információért írja be a következőt: `Get-Help Get-Credential` .

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
Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.
Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.
A bináris tömb maximális hossza 65535 bájt.<br>
**Megjegyzés: ne adjon meg semmilyen titkot vagy jelszót a customData tulajdonságban.**<br>
Ez a tulajdonság nem frissíthető a VM létrehozása után. <br>
a customData-ra a program a VM-re továbbítja a fájlt, további információt az [Egyéni adatok az Azure VMS](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) szolgáltatásban című témakörben talál. <br>
A Cloud-init for your Linux VM használata esetén olvassa el a következő témakört: a [Cloud-init használata a Linux VM testreszabására a létrehozás során](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Tiltsa le a létesítés VM Agent-ügynököt.

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
Jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.

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
Itt adhatja meg a IaaS virtuális gépre való frissítésének módját.<br><br>
A lehetséges értékek a következők:<br>
**Manuális** : a javítások alkalmazását egy virtuális gépre irányítja. Ezt úgy teheti meg, hogy a VM-ben manuálisan alkalmazza a tapaszokat. Ebben az üzemmódban az automatikus frissítések le vannak tiltva; a WindowsConfiguration. enableAutomaticUpdates tulajdonságnak false-nak kell lennie.<br>
**AutomaticByOS** – a virtuális gépet automatikusan frissíti az operációs rendszer. A WindowsConfiguration. enableAutomaticUpdates tulajdonságnak igaznak kell lennie. <br >
**AutomaticByPlatform** – a virtuális gépet automatikusan frissíti az operációs rendszer. A provisionVMAgent és a WindowsConfiguration. enableAutomaticUpdates tulajdonságnak igaznak kell lennie

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
Azt jelzi, hogy a beállítások megkövetelik, hogy a virtuálisgép-ügynök telepítve legyen a virtuális gépre.

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

### -Időzóna
A virtuális gép időzónáját adja meg. például \" Pacific standard Time \" . <br>
A lehetséges értékek a [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)által eredményül adott időzónákban is [TimeZoneInfo.id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) .

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
Annak a helyi virtuális gépnek az objektumát adja meg, amelybe az operációs rendszer tulajdonságait be szeretné állítani.
A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.
Virtuális gép objektum létrehozása az New-AzVMConfig parancsmag használatával.

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
Azt jelzi, hogy a Windows operációs rendszer típusa.

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
A WinRM-tanúsítványok URI-azonosítóját adja meg.
Ezt egy fontos boltozaton kell tárolni.

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
Azt jelzi, hogy az operációs rendszer a HTTP WinRM szolgáltatást használja.

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
Azt jelzi, hogy ez az operációs rendszer HTTPS-WinRM protokollt használ.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

### System. Management. Automation. SwitchParameter

### System. String

### System. Management. Automation. PSCredential

### System. URI

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Új – AzVMConfig](./New-AzVMConfig.md)


