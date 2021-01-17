---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469882"
---
# Get-AzEventHubConsumerGroup

## SYNOPSIS
Lekérte egy adott Eseményközpont fogyasztói csoportjának adatait, vagy lekérte egy fogyasztói csoportok listáját az Eseményközpontban.

## SZINTAXIS

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzEventHubConsumerGroup parancsmag vagy egy megadott Event Hubs fogyasztói csoport adatait, vagy egy adott eseményközpont fogyasztói csoportjainak listáját kapja meg.
Ha meg van biztosítanak egy fogyasztói csoport nevét, egyetlen fogyasztói csoport adatait is visszaadja a szolgáltatás.
Ha nincs megadva egy fogyasztói csoport neve, a megadott Eseményközpontban visszaadja a fogyasztói csoportok listáját.

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

A MyConsumerGroupName fogyasztói csoportot beveszi az Event Hub MyEventHubName eseményközpontba, amely a MyNamespaceName nevű névtérben létezik a \` \` \` \` \` \` \` MyResourceGroupName \` erőforráscsoporttal.

### 2. példa
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

A \` \` \` \` \` MyResourceGroupName erőforráscsoport myResourceGroupName nevű erőforráscsoportjával a MyNamespaceName névterében található, az Event Hub MyEventHubName nevű fogyasztói csoportjainak listáját \` tartalmazza.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHub
EventHub neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Határozza meg, hogy legfeljebb hány ConsumerGroups csoportot kell visszaadni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
ConsumerGroup Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
