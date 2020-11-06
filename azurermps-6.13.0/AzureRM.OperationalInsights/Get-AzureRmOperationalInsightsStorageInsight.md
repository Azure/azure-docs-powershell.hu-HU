---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: b0d3baaa1e41e6f0df74e1b6bf39bdc858777a92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491888"
---
# Get-AzureRmOperationalInsightsStorageInsight

## Áttekintés
Információt kap a tárterület-betekintésről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByWorkspaceName (alapértelmezett)
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmOperationalInsightsStorageInsight** parancsmag információkat kap a meglévő tárterület-betekintésről.
Ha meg van adva egy tárterület-betekintési név, ez a parancsmag információkat kap a tárterületről.
Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterületen található összes tárterületről.

## Példák

### Példa 1: tárterület-betekintést kaphat név szerint
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Ez a parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a ContosoWorkspace nevű munkaterületről.

### 2. példa: tárterület betekintésének beszerzése munkaterület-objektum használatával
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

Az első parancs a **Get-AzureRmOperationalInsightsWorkspace** parancsmagot használja az üzemeltetési környezetek munkaterületének beszerzéséhez, majd a $Workspace változóban tárolja.
A második parancs beolvassa a MyStorageInsight nevű tárterület-betekintést a $Workspace munkaterületéhez.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
A tárterület-betekintési nevet adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Munkaterület
A tárolási környezeteket tartalmazó munkaterületet adja meg.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
A tárolási állapotot tartalmazó munkaterület nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace
Paraméterek: munkaterület (ByValue)

### System. String

## KIMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSStorageInsight

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure hadműveleti parancsmagok](./AzureRM.OperationalInsights.md)


