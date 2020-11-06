---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 7da7382359202f3856309c24a3ea484bd9b3e9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493019"
---
# Set-AzureRmSchedulerServiceBusTopicJob

## Áttekintés
Egy szolgáltatási busz témakörének módosítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmSchedulerServiceBusTopicJob** parancsmag az Azure Scheduler szolgáltatásban módosítja a szolgáltatási busz témakört.

Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.
A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.

Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.
Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.

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

### -A befejezési időpont
A projekthez tartozó **datetime** -objektum záró időpontját adja meg.
Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionType
A feladat hibaérték-beállítását adja meg.
A paraméter elfogadható értékei a következők:

- Http 
- Https 
- StorageQueue 
- ServiceBusQueue 
- ServiceBusTopic

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExecutionCount
Itt adhatja meg, hogy hányszor fusson a feladat.
Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gyakoriság
A feladat maximális gyakoriságát adja meg.
A paraméter elfogadható értékei a következők:

- Perces 
- Óra 
- Nap 
- Héten 
- Hónap

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intervallum
A feladat ismétlődésének intervallumát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Annak a feladatnak a neve, amelyhez a projekt tartozik.

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
Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.

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

### -JobState
A feladat állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Engedélyezve 
- Tiltva

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.

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

### -ServiceBusMessage
A szolgáltatás buszjának témáját tartalmazó üzenetet adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
A szolgáltatás busz-névteret adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusSasKeyName
Egy megosztott Access-aláírási kulcs nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusSasKeyValue
A megosztott hozzáférés-aláírási kulcs értékét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusTopicPath
A szolgáltatás buszja témakör elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusTransportType
A szolgáltatás busz-átviteli típusát adja meg.
A paraméter elfogadható értékei a következők:

- NetMessaging
- AMQP

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kezdő időpont
A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmSchedulerHttpJob](./New-AzureRmSchedulerHttpJob.md)

[Új – AzureRmSchedulerJobCollection](./New-AzureRmSchedulerJobCollection.md)

[Új – AzureRmSchedulerServiceBusQueueJob](./New-AzureRmSchedulerServiceBusQueueJob.md)

[Új – AzureRmSchedulerServiceBusTopicJob](./New-AzureRmSchedulerServiceBusTopicJob.md)

[Új – AzureRmSchedulerStorageQueueJob](./New-AzureRmSchedulerStorageQueueJob.md)

[Set-AzureRmSchedulerHttpJob](./Set-AzureRmSchedulerHttpJob.md)

[Set-AzureRmSchedulerJobCollection](./Set-AzureRmSchedulerJobCollection.md)

[Set-AzureRmSchedulerServiceBusQueueJob](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[Set-AzureRmSchedulerStorageQueueJob](./Set-AzureRmSchedulerStorageQueueJob.md)


