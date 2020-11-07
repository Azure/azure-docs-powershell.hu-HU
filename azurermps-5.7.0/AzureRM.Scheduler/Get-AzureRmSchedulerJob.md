---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679706"
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

### -JobCollectionName
Annak a webhelycsoporthoz a nevét adja meg, amely a beszerzéshez feladatokat tartalmaz.

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

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


