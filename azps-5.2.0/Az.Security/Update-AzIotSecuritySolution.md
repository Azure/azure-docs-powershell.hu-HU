---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353670"
---
# Update-AzIotSecuritySolution

## SYNOPSIS
Az IoT biztonsági megoldásában a következő tulajdonságok frissítése: címkék, ajánlott konfiguráció, felhasználó által definiált erőforrások

## SZINTAXIS

### ResourceGroupLevelResource (alapértelmezett)
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Update-AzIotSecuritySolution egy adott IoT-biztonsági megoldásban a következő tulajdonságok közül egy vagy több tulajdonságokkal rendelkezik: címkék, ajánlott konfiguráció, felhasználó által definiált erőforrások.
Csak a megadott tulajdonságok frissülnek az iot biztonsági megoldáson belül.
Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

A MySample biztonsági megoldás "MySample" frissítése a "MyResourceGroup" erőforráscsoportból ajánlott konfigurációval és felhasználó által definiált erőforrásokkal

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

### -InputObject
Bemeneti objektum.

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Erőforrás neve.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecommendationsConfiguration
Javaslatok konfiguráció.

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Címkék.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDefinedResource
Felhasználó által definiált erőforrások.

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSUserDefinedResources

### Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSRecommendationConfiguration[]

## KIMENETEK

### Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
