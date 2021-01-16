---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366993"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Beállítja a VMSS operációs rendszer profiltulajdonságokat.

## SZINTAXIS

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVmssOsProfile** parancsmag beállítja az operációs rendszer profiltulajdonságokat.

## PÉLDÁK

### 1. példa: Az operációs rendszer profiltulajdonságának beállítása VMSS-hez
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Ez a parancs beállítja a ContosoVMSS nevű VMSS-hez tartozó virtuális gépek operációs rendszerprofil-tulajdonságait.
A parancs a VMSS összes virtuális géppéldányának számítógépnév-előtagját beállítja tesztelésre, és megadja a rendszergazdai felhasználónevet és jelszót.

## PARAMETERS

### -AdditionalUnattendContent
Felügyelet nélküli tartalomobjektumot ad meg.
A Add-AzVMAdditionalUnattendContent létrehozhatja az objektumot.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Megadja azt a rendszergazdai jelszót, amely a VMSS összes virtuális gépi példányához használható.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Megadja azt a rendszergazdai fióknevet, amely a VMSS összes virtuális gépi példányában használható. <br>
**Windowsos korlátozás:** Nem végződhet \" a következőre: .\" <br>
**Nem engedélyezett értékek:** \" \"rendszergazda, \" \" rendszergazda, \" \" felhasználó, \" \" felhasználó1, \" \" teszt, \" \" felhasználó2, \" \" teszt1, \" \" felhasználó3, \" \" rendszergazda1, \" \" 1, \" 123, \" a , \" \" \" actuser, \" \" adm, \" \" \" admin2, \" aspnet, \" \" \" backup, \" \" console, david , \" \" \" \" guest, \" \" john, \" \" owner, \" \" root, \" \" server, \" \" \" \" sql, support, \" \" support_388945a0, \" \" sys, \" \" test2, \" \" \" test3, \" felhasználó4, \" \" user5. <br>
**Minimális hossz (Linux):** 1 karakter <br>
**Max-length (Linux):** 64 karakter <br>
**Max-length (Windows):** 20 karakter  <br>
<li> A Linux VM-hez való root hozzáférésről a Root jogosultságok használata [Linux-virtuális gépeken az Azure-ban.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> A Linux rendszerben olyan beépített felhasználók listáját, akik nem használhatók ebben a mezőben, az [Azure-ban](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)a Linux-felhasználók nevének kiválasztása.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
A VMSS-ban található összes virtuális géppéldány számítógépnév-előtagját adja meg.
A számítógép nevének 1–15 karakter hosszúnak kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Egy 64-es alapkódolt egyéni adatokat kódolt karakterláncot ad meg.
Ezt egy bináris tömbbe dekódolja, amely fájlként van mentve a virtuális gépre.
A bináris tömb maximális hossza 65535 bájt. <br>
Ha felhőbeli initet használ a VIRTUÁLIS GÉPhez, tekintse meg a Linux-virtuális gép testreszabása [felhőbeli init használatával a készítés során.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -LinuxConfigurationDisablePasswordAuthentication
Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
A Windows Remote Management (WinRM) hallgatóit határozza meg.
Ez lehetővé teszi a távoli Windows PowerShellt.
A Add-AzVmssWinRMListener létrehozhatja a hallgatót.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
A Biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektum megadása.
Az objektum létrehozásához használhatja Add-AzVMSshPublicKey parancsmagot.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Megadja a virtuális gépen található tanúsítványhivatkozásokat tartalmazó titkos objektumokat.
A titkos Add-AzVmssSecret objektum létrehozásához használhatja a Add-AzVmssSecret parancsmagot.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
A virtuális gép időzónáját határozza meg. például a \" csendes-óceáni téli \" idő. <br>
A lehetséges értékek a [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [által visszaadott](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) időzónákból származó TimeZoneInfo.Id is beállíthatók.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
A VMSS-objektumot adja meg.
Az objektum létrehozásához használhatja New-AzVmssConfig parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Azt jelzi, hogy a VMSS virtuális gépei engedélyezve vannak-e az automatikus frissítésekhez.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Azt jelzi, hogy a virtuális gép ügynökét a VMSS virtuális gépeinél kell-e kiépítenünk.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


