---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680177"
---
# Set-AzureRmVmssOsProfile

## Áttekintés
Beállítja a VMSS operációs rendszer profiljának tulajdonságait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVmssOsProfile** parancsmag a virtuális gép méretarányának beállítása operációs rendszer profiljának tulajdonságait adja meg.

## Példák

### Példa 1: az operációs rendszer profiljának tulajdonságainak beállítása VMSS
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Ez a parancs beállítja az operációs rendszer profiljának tulajdonságait a ContosoVMSS nevű VMSS tartozó virtuális gépekhez.
A parancs a VMSS a virtuálisgép-példányok számítógép nevének előtagját állítja be a rendszergazda felhasználónevének és jelszavának teszteléséhez és ellátásához.

## PARAMÉTEREK

### -AdditionalUnattendContent
Egy felügyelet nélküli tartalom-objektumot ad meg.
Az objektum létrehozásához használhatja a Add-AzureRmVMAdditionalUnattendContent.

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
A VMSS lévő összes virtuálisgép-példányhoz használt rendszergazdai jelszót adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Annak a rendszergazdai fióknak a nevét adja meg, amelyet a VMSS minden virtuális gép példányához használni szeretne.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
A VMSS a virtuálisgép-példányok számítógép nevének előtagját adja meg.
A számítógépek nevének 1 – 15 karakter hosszúnak kell lennie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.
Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.
A bináris tömb maximális hossza 65535 bájt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LinuxConfigurationDisablePasswordAuthentication
Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
A Windows Remote Management (WinRM) figyelőit adja meg.
Ez engedélyezi a távoli Windows PowerShellt.
A figyelő létrehozásához használhatja a Add-AzureRmVmssWinRMListener parancsmagot.

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
A biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektumát adja meg.
Az objektum létrehozásához az Add-AzureRmVMSshPublicKey parancsmagot használhatja.

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Megadja a titok objektumot, amely a virtuális gépen elhelyezni kívánt tanúsítványra mutató hivatkozásokat tartalmazza.
A Secrets objektumot a Add-AzureRmVmssSecret parancsmaggal hozhatja létre.

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Időzóna
A virtuális gép időzónáját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
A VMSS objektumot adja meg.
Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Azt jelzi, hogy a VMSS lévő virtuális gépek engedélyezve vannak-e az automatikus frissítésekhez.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Azt jelzi, hogy a virtuális gép ügynököt kell-e kiépíteni a VMSS lévő virtuális gépeken.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmVMAdditionalUnattendContent](./Add-AzureRmVMAdditionalUnattendContent.md)

[Add-AzureRmVmssWinRMListener](./Add-AzureRmVmssWinRMListener.md)

[Add-AzureRmVMSshPublicKey](./Add-AzureRmVMSshPublicKey.md)

[Add-AzureRmVmssSecret](./Add-AzureRmVmssSecret.md)

[Új – AzureRmVmssConfig](./New-AzureRmVmssConfig.md)


