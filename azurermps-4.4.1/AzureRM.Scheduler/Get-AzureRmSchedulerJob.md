---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679334"
---
# Get-AzureRmSchedulerJob

## Áttekintés
A Feladatütemező munkalapjait kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSchedulerJob** parancsmag Azure Scheduler-feladatokat kap.

## Példák

## PARAMÉTEREK

### -JobCollectionName
Annak a webhelycsoporthoz a nevét adja meg, amely a beszerzéshez feladatokat tartalmaz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Feladatnév
A beolvasott feladat nevét adja meg.

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

### -JobState
A beolvasott feladatok állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Engedélyezve 
- Tiltva 
- Hibázott 
- Kész

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A beolvasott feladatok erőforráscsoport részét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmSchedulerHttpJob](./New-AzureRmSchedulerHttpJob.md)

[Új – AzureRmSchedulerJobCollection](./New-AzureRmSchedulerJobCollection.md)

[Új – AzureRmSchedulerServiceBusQueueJob](./New-AzureRmSchedulerServiceBusQueueJob.md)

[Új – AzureRmSchedulerServiceBusTopicJob](./New-AzureRmSchedulerServiceBusTopicJob.md)

[Új – AzureRmSchedulerStorageQueueJob](./New-AzureRmSchedulerStorageQueueJob.md)

[Remove-AzureRmSchedulerJob](./Remove-AzureRmSchedulerJob.md)

[Set-AzureRmSchedulerHttpJob](./Set-AzureRmSchedulerHttpJob.md)

[Set-AzureRmSchedulerServiceBusQueueJob](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[Set-AzureRmSchedulerServiceBusTopicJob](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[Set-AzureRmSchedulerStorageQueueJob](./Set-AzureRmSchedulerStorageQueueJob.md)


