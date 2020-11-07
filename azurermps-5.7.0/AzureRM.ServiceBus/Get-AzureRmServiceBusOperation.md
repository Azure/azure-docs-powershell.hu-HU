---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679703"
---
# Get-AzureRmServiceBusOperation

## Áttekintés
Támogatott ServiceBus-műveletek listája

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmServiceBusOperation** parancsmag a támogatott ServiceBus-műveleteket jeleníti meg.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmServiceBusOperation
```

A ServiceBus által támogatott műveletek listája

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSOperationAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.4.2.0, Culture = semleges, PublicKeyToken = null]]

## KIMENETEK

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ServiceBus. models. OperationAttributes]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

