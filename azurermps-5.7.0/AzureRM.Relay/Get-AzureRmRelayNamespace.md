---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679721"
---
# Get-AzureRmRelayNamespace

## Áttekintés
A megadott továbbítási névtér leírását kapja az erőforráscsoport között.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRelayNamespace** parancsmag leírását kapja a megadott továbbítási névtérhez az erőforráscsoporten belül.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

A megadott továbbítási névtér leírását adja meg.

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
A továbbító névtér neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -ResourceGroupName
System. String

### -Name (név)
 System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. RelayNamespaceAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]
ProvisioningState: sikeres CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-relay1: West US Tags: {[Tag1, Tag1Value]} ID: TestNameSpace-Relay1/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

