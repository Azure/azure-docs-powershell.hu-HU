---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 7fc2777f4ab7f64aea4accb22d30f7df54c1476a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666528"
---
# Get-AzEventGridTopicType

## Áttekintés
Az Azure Event Grid által támogatott témák részleteit kapja meg.

## SZINTAXISA

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az Azure Event Grid által támogatott témakörök részleteit kapja meg.
Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.
Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.
Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

A témakör típusainak listáját kapja.

### 2. példa
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Információt kap a StorageAccounts témakör típusáról.

### 3. példa
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -IncludeEventTypeData
Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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

## KIMENETEK

### Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance

### Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
