---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502580"
---
# Get-AzureRmEventHubNamespace

## Áttekintés
Beolvassa az esemény-hubok névterének részleteit, vagy az aktuális Azure-előfizetésből az összes esemény-hubok névterének listáját kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzureRmEventHubNamespace parancsmag az aktuális Azure-előfizetésben lévő adott esemény-hubok névterének részleteit vagy az összes esemény hubok névterét tartalmazza.
Ha a névtér neve meg van határozva, az egyetlen esemény-hubok névtér részleteit adja vissza a rendszer.
Ha a névtér neve nincs megadva, a program a névterek listáját adja vissza.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Az esemény-hubok névtér-MyNamespaceName részleteit kapja \` \` meg az erőforráscsoport \` MyResourceGroupName \` .

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
EventHub-névtér neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction
További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String


## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
