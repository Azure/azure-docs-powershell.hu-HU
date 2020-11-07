---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672194"
---
# Get-AzureRmServiceBusNamespace

## Áttekintés
A megadott szolgáltatási busz névterének leírását adja meg az erőforráscsoport között.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmServiceBusNamespace** parancsmag leírását kapja a megadott szolgáltatási busz névtérhez az erőforrás csoportban.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

A megadott szolgáltatási busz névterének leírását adja meg.

## PARAMÉTEREK

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

### -Name (név)
Névtér neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -ResourceGroup
System. String

### -NamespaceName
 System. String

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. NamespaceAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]
Név: SB-Example1 azonosító:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 hely: Nyugat-amerikai SKU: név: standard, kapacitás: 1, Tier: standard ProvisioningState: örökölt állapot: Active CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ enabled: true

## MEGJEGYZI
## KAPCSOLÓDÓ HIVATKOZÁSOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

