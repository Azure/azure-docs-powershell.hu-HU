---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493311"
---
# Get-AzureRmStreamAnalyticsQuota

## Áttekintés
Információt kap egy régió streaming Unit kvótáról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmStreamAnalyticsQuota** parancsmag információkat kap egy adott terület adatfolyam-kvótáról.

## Példák

### 1. példa: információk beszerzése egy régió streaming Unit kvótáról
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

Ez a parancs információt ad eredményül a folyó egység kvótáról és használatáról a Nyugat-amerikai régióban.

## PARAMÉTEREK

### -Hely
Itt adhatja meg egy Azure-terület vagy adatközpont-hely nevét, amelyhez adatfolyam-kvóta adatait szeretne beszerezni.
Lásd: https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services támogatott Azure-régiók listája.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSQuota, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSQuota

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure stream Analytics-parancsmagok](./AzureRM.StreamAnalytics.md)


