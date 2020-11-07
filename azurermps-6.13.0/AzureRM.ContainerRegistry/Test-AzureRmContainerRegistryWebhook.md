---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672314"
---
# Test-AzureRmContainerRegistryWebhook

## Áttekintés
Elindítja a webhook ping eseményt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ResourceIdParameterSet (alapértelmezett)
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### NameResourceGroupParameterSet
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WebhookObjectParameterSet
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Test-AzureRmContainerRegistryWebhook parancsmag a webhook ping eseményét indítja el.

## Példák

### Példa 1: webhook-ping-esemény indítja el.
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

Elindítja a webhook ping eseményt.

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
Webhook-név.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryName
A tároló beállításjegyzékének neve.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A Container Registry webhook-erőforrás azonosítója

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Webhook
Tároló rendszerleíróadatbázis-objektum.

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryWebhook
Paraméterek: webhook (ByValue)

### System. String

## KIMENETEK

### Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryEventInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmContainerRegistryWebhook](New-AzureRmContainerRegistryWebhook.md)

[Get-AzureRmContainerRegistryWebhook](Get-AzureRmContainerRegistryWebhook.md)

[Update-AzureRmContainerRegistryWebhook](Update-AzureRmContainerRegistryWebhook.md)

[Remove-AzureRmContainerRegistryWebhook](Remove-AzureRmContainerRegistryWebhook.md)
