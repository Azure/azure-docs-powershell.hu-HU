---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503879"
---
# Get-AzureRmBillingPeriod

## Áttekintés
Az előfizetés számlázási időszakának beszerzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Egyetlen
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBillingPeriod** parancsmag az előfizetés számlázási időszakait kapja meg.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Az előfizetés összes rendelkezésre álló számlázási időszakának beszerzése.

### 2. példa
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

A megadott nevű előfizetés számlázási időszakának beszerzése

### 3. példa
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Az előfizetés legfeljebb 2 számlázási időszakának beszerzése

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -MaxCount
Adja meg, hogy legfeljebb hány rekordot szeretne megadni.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beszerzéshez megadott számlázási időszak neve.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. számlázás. models. PSBillingPeriod, Microsoft. Azure. commands. számlázás, verzió = 0.14.0.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

