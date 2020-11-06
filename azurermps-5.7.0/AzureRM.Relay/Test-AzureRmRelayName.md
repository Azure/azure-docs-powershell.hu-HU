---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498871"
---
# Test-AzureRmRelayName

## Áttekintés
A megadott névtér-név elérhetőségének ellenőrzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **teszt-AzureRmRelayName** parancsmag a névtér nevének elérhetőségét ellenőrzi

## Példák

### Példa 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### 2. példa
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### 3. példa
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

A névtér nevében elérhető állapotot adja eredményül.

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

### -Namespace
A továbbító névtér neve

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

### [Microsoft. Azure. Command. Relay. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]

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

