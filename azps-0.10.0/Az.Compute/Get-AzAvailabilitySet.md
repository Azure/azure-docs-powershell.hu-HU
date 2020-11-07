---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844673"
---
# Get-AzAvailabilitySet

## Áttekintés
Az Azure elérhetőségi készleteit egy erőforráscsoport kapja meg.

## SZINTAXISA

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzAvailabilitySet** parancsmag az Azure elérhetőségi készleteit egy erőforráscsoport szerint kapja meg.
Megadhatja a beszerzéshez megadott elérhetőségi készlet nevét.

## Példák

### Példa 1: meghatározott elérhetőségi halmaz beszerzése
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

Ez a parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforrás-csoport elérhetőségi készletét.

### 2. példa: az összes elérhetőségi készlet beszerzése
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

Ez a parancs a ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A parancsmag által beolvasott elérhetőségi készlet nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzAvailabilitySet](./New-AzAvailabilitySet.md)

[Remove-AzAvailabilitySet](./Remove-AzAvailabilitySet.md)


