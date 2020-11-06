---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: e1701d60289343bb61a2891617fd10c6b9987b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504995"
---
# Get-AzureRmHDInsightProperties

## Áttekintés
Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmHDInsightProperties** parancsmag az Azure HDInsight-ra jellemző tulajdonságokat kapja meg, például az elérhető helyek listáját, a HDInsight, valamint a rendelkezésre álló számítási kapacitást.

## Példák

### Példa 1: az Azure HDInsight-fürtök tulajdonságainak beszerzése
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

Ez a parancs egy HDInsight-szolgáltatás tulajdonságainak beolvasása a kelet-amerikai (2) helyről.

## PARAMÉTEREK

### -Hely
Annak a helynek a helye, ahol a HDInsight tulajdonságait le szeretné olvasni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

## KIMENETEK

### Microsoft. Azure. Management. HDInsight. models. CapabilitiesResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

