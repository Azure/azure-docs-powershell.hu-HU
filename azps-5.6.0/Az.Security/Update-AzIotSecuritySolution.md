---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: aec6fb98b5894b075cea7cf9b087b9f9c042779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005717"
---
# <span data-ttu-id="47dbf-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47dbf-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="47dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="47dbf-103">Az IoT biztonsági megoldásában a következő tulajdonságok frissítése: címkék, ajánlott konfiguráció, felhasználó által definiált erőforrások</span><span class="sxs-lookup"><span data-stu-id="47dbf-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="47dbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47dbf-104">SYNTAX</span></span>

### <span data-ttu-id="47dbf-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47dbf-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47dbf-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47dbf-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47dbf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="47dbf-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dbf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47dbf-108">DESCRIPTION</span></span>
<span data-ttu-id="47dbf-109">A Update-AzIotSecuritySolution egy adott IoT-biztonsági megoldásban a következő tulajdonságok közül egy vagy több tulajdonságokkal rendelkezik: címkék, ajánlott konfiguráció, felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="47dbf-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="47dbf-110">Csak a megadott tulajdonságok frissülnek az iot biztonsági megoldáson belül.</span><span class="sxs-lookup"><span data-stu-id="47dbf-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="47dbf-111">Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="47dbf-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="47dbf-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47dbf-112">EXAMPLES</span></span>

### <span data-ttu-id="47dbf-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="47dbf-113">Example 1</span></span>
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

<span data-ttu-id="47dbf-114">A MySample biztonsági megoldás "MySample" frissítése a "MyResourceGroup" erőforráscsoportból ajánlott konfigurációval és felhasználó által definiált erőforrásokkal</span><span class="sxs-lookup"><span data-stu-id="47dbf-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="47dbf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47dbf-115">PARAMETERS</span></span>

### <span data-ttu-id="47dbf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dbf-116">-DefaultProfile</span></span>
<span data-ttu-id="47dbf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47dbf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47dbf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47dbf-118">-InputObject</span></span>
<span data-ttu-id="47dbf-119">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="47dbf-119">Input Object.</span></span>

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

### <span data-ttu-id="47dbf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="47dbf-120">-Name</span></span>
<span data-ttu-id="47dbf-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47dbf-121">Resource name.</span></span>

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

### <span data-ttu-id="47dbf-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="47dbf-123">Javaslatok konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="47dbf-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="47dbf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dbf-124">-ResourceGroupName</span></span>
<span data-ttu-id="47dbf-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47dbf-125">Resource group name.</span></span>

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

### <span data-ttu-id="47dbf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47dbf-126">-ResourceId</span></span>
<span data-ttu-id="47dbf-127">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="47dbf-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="47dbf-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="47dbf-128">-Tag</span></span>
<span data-ttu-id="47dbf-129">Címkék.</span><span class="sxs-lookup"><span data-stu-id="47dbf-129">Tags.</span></span>

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

### <span data-ttu-id="47dbf-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="47dbf-130">-UserDefinedResource</span></span>
<span data-ttu-id="47dbf-131">Felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="47dbf-131">User defined resources.</span></span>

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

### <span data-ttu-id="47dbf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47dbf-132">-Confirm</span></span>
<span data-ttu-id="47dbf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47dbf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47dbf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dbf-134">-WhatIf</span></span>
<span data-ttu-id="47dbf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47dbf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47dbf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47dbf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47dbf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dbf-137">CommonParameters</span></span>
<span data-ttu-id="47dbf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dbf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dbf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47dbf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dbf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47dbf-140">INPUTS</span></span>

### <span data-ttu-id="47dbf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="47dbf-141">System.String</span></span>

### <span data-ttu-id="47dbf-142">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47dbf-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="47dbf-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="47dbf-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47dbf-144">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="47dbf-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="47dbf-145">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="47dbf-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="47dbf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47dbf-146">OUTPUTS</span></span>

### <span data-ttu-id="47dbf-147">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47dbf-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="47dbf-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47dbf-148">NOTES</span></span>

## <span data-ttu-id="47dbf-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47dbf-149">RELATED LINKS</span></span>
