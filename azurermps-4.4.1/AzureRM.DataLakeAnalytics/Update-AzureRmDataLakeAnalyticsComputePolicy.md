---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502748"
---
# Update-AzureRmDataLakeAnalyticsComputePolicy

## Áttekintés
Az adattó-elemzés frissíti egy adott AAD-entitásra vonatkozó házirend-szabályt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Update-AzureRmDataLakeAnalyticsComputePolicy** frissíti az Azure Data Lake-beli Analytics-fiókban meghatározott aad-entitásokra vonatkozó meghatározott számítási házirend-szabályt.

## Példák

### Példa 1: egy szabály frissítése egy számítási házirendben
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

Ez a parancs frissíti a "contosoadla" fiók "myPolicy" nevű házirendjét, így biztosítva, hogy a felhasználó nem tud több mint 5 párhuzamosan elküldeni a munkát.

### 2. példa: számítási házirend létrehozása a szabályok frissítésével
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban, hogy a felhasználó nem tud több mint 5 párhuzamosságtal vagy a 100-nál kisebb prioritással elküldenie a munkát.

## PARAMÉTEREK

### -Fiók
Annak a fióknak a neve, amely frissíti a számítási házirendet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxDegreeOfParallelismPerJob
A párhuzamosságok maximálisan támogatott foka ebben a házirendben. Ezt, MinPriorityPerJob vagy mindkét paramétert meg kell adni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
A házirendre vonatkozó, a minimálisan támogatott prioritás. Ezt, MaxDegreeOfParallelismPerJob vagy mindkét paramétert meg kell adni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak a számítási házirendnek a neve, amelyet frissíteni szeretne.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.
Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
System. Int32

## KIMENETEK

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

