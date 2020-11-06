---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493180"
---
# Set-AzureRmVMBginfoExtension

## Áttekintés
A BGInfo bővítmény felvétele egy virtuális gépre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVMBGInfoExtension** parancsmag hozzáadja a BGInfo bővítményt egy virtuális géphez.

## Példák

### Példa 1: a BGInfo bővítmény felvétele egy virtuális gépre
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
Ez a parancs hozzáadja a BGInfo bővítményt egy ContosoVM nevű virtuális géphez az erőforráscsoport ContosoRG.

### 2. példa: a BGInfo bővítmény adott verziójának hozzáadása egy virtuális géphez
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

Ez a parancs hozzáadja a BGInfo bővítményt a ContosoVM nevű virtuális géphez.
A parancs a virtuális gép erőforrás csoportját és helyét adja meg.
A parancs a bővítmény nevét és verziószámát adja meg.

## PARAMÉTEREK

### -DisableAutoUpgradeMinorVersion
Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményt egy újabb alverzióra.
Ez a parancsmag alapértelmezés szerint lehetővé teszi, hogy a Guest Agent frissítse a bővítményt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Azt adja meg, hogy a bővítményt ugyanazzal a nyilvános vagy védett beállításokkal kell futtatni.
Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.

Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
A virtuális gép helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Megadja annak a BGInfo-kiterjesztésnek a nevét, amelyet a parancsmag a virtuális gépre ad.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a virtuális gépnek az erőforráscsoport nevét adja meg, amelyre a parancsmag hozzáadja a bővítményt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Annak a bővítménynek a verziószámát adja meg, amelyet a parancsmag a virtuális gépre ad.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a neve, amelyhez a parancsmag hozzáadja az BGInfo bővítményt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.

A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

