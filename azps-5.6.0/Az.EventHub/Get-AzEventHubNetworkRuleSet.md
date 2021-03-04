---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921218"
---
# Get-AzEventHubNetworkRuleSet

## SYNOPSIS
Az aktuális Azure-előfizetés névterének Event Hubs NetworkruleSet-ének adatait tartalmazza.

## SZINTAXIS

### NetworkRuleSetPropertiesSet (alapértelmezett)
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NetworkRuleSetNamespacePropertiesSet
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### NetworkRuleSetResourceIdParameterSet
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Az aktuális Azure-előfizetés névterének Event Hubs NetworkruleSet-ének adatait tartalmazza.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

Az Event Hubs NetworkruleSet névtérről a ResourceGroup és a Namespace paramétereit használva olvashatja le a részleteket. 

### 2. példa
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

Az aktuális előfizetésben lévő Namespace segítségével lekérte az Event Hubs NetworkruleSet névterének részleteit.

### 3. példa
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

Az Event Hubs NetworkruleSet névtérről, más névtér erőforrás-azonosítójával 

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Namespace
Namespace Name

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Namespace Resource Id

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.
További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK