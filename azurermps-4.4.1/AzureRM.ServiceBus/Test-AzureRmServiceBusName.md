---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679935"
---
# Test-AzureRmServiceBusName

## Áttekintés
A megadott névtér-név elérhetőségének ellenőrzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## Leírás
A **teszt-AzureRmServiceBusName** parancsmag a névtér nevének elérhetőségét ellenőrzi

## Példák

### Példa 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### 2. példa
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### 3. példa
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

A névtér nevében elérhető állapotot adja eredményül.

## PARAMÉTEREK

### -Namespace
ServiceBus-névtér neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -Namespace
 System. String

## KIMENETEK

### [Microsoft. Azure. Command. ServiceBus. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]

### Példa 1
NameAvailable-ok üzenet
------------- ------ -------
         True   None

### 2. példa
NameAvailable-ok üzenet
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### 3. példa
NameAvailable-ok üzenet
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
