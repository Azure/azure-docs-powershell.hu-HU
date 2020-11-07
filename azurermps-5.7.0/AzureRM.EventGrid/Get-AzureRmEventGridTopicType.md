---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: bc272648920e29ed2e735ca08b9fa78563a9f9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673062"
---
# Get-AzureRmEventGridTopicType

## Áttekintés
Az Azure Event Grid által támogatott témák részleteit kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az Azure Event Grid által támogatott témakörök részleteit kapja meg.
Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.
Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.
Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventGridTopicType
```

A témakör típusainak listáját kapja.

### 2. példa
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Információt kap a StorageAccounts témakör típusáról.

### 3. példa
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -IncludeEventTypeData
Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
EventGrid a téma típusa név.

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

### System. String
System. Management. Automation. SwitchParameter

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance, Microsoft. Azure. commands. EventGrid, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

