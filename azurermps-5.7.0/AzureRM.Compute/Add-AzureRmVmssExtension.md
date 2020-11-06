---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492390"
---
# Add-AzureRmVmssExtension

## Áttekintés
Hozzáad egy bővítményt a VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).

## Példák

### 1. példa: bővítmény felvétele a VMSS
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

Ez a parancs bővítményt ad a VMMS.

## PARAMÉTEREK

### -AutoUpgradeMinorVersion
Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.

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

### -Name (név)
Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.

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

### -ProtectedSetting
A bővítmény privát konfigurációját adja meg karakterláncként.
Ez a parancsmag titkosítja a magánjellegű konfigurációt.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
A bővítmény közzétevőének nevét adja meg.
A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.
Ez a [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.

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

### -Beállítás
Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.
Ez a parancsmag nem titkosítja a nyilvános konfigurációt.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type (típus)
A bővítmény típusát adja meg.
A [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.

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

### -TypeHandlerVersion
Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.
A [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.

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

### -VirtualMachineScaleSet
Adja meg a VMSS objektumot.
Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .

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

###  
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRmVmssExtension](./Remove-AzureRmVmssExtension.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[Új – AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
