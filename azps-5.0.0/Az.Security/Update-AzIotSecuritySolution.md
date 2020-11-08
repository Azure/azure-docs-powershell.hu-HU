---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186180"
---
# <span data-ttu-id="794bd-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="794bd-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="794bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="794bd-102">SYNOPSIS</span></span>
<span data-ttu-id="794bd-103">Frissítse a következő tulajdonságokat a IoT biztonsági megoldásban: címkék, ajánlás-konfiguráció, felhasználó által definiált erőforrások</span><span class="sxs-lookup"><span data-stu-id="794bd-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="794bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="794bd-104">SYNTAX</span></span>

### <span data-ttu-id="794bd-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="794bd-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794bd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="794bd-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794bd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="794bd-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794bd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="794bd-108">DESCRIPTION</span></span>
<span data-ttu-id="794bd-109">A Update-AzIotSecuritySolution parancsmag az alábbi updayes közül legalább egy adott IoT biztonsági megoldást tartalmaz: címkék, ajánlás-konfiguráció, felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="794bd-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="794bd-110">A IOT biztonsági megoldásban csak a megadott tulajdonságok lesznek frissítve.</span><span class="sxs-lookup"><span data-stu-id="794bd-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="794bd-111">A IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt a IoT-eszközökről és a IoT hub-ról a fenyegetések megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="794bd-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="794bd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="794bd-112">EXAMPLES</span></span>

### <span data-ttu-id="794bd-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="794bd-113">Example 1</span></span>
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

<span data-ttu-id="794bd-114">A "MySample" IOT biztonsági megoldásának frissítése a "MyResourceGroup" erőforráscsoporthoz "az ajánlás konfigurációja és a felhasználó által definiált erőforrásokkal"</span><span class="sxs-lookup"><span data-stu-id="794bd-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="794bd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="794bd-115">PARAMETERS</span></span>

### <span data-ttu-id="794bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794bd-116">-DefaultProfile</span></span>
<span data-ttu-id="794bd-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="794bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="794bd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="794bd-118">-InputObject</span></span>
<span data-ttu-id="794bd-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="794bd-119">Input Object.</span></span>

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

### <span data-ttu-id="794bd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="794bd-120">-Name</span></span>
<span data-ttu-id="794bd-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="794bd-121">Resource name.</span></span>

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

### <span data-ttu-id="794bd-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="794bd-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="794bd-123">Javaslatok konfigurálása</span><span class="sxs-lookup"><span data-stu-id="794bd-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="794bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="794bd-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="794bd-125">Resource group name.</span></span>

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

### <span data-ttu-id="794bd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="794bd-126">-ResourceId</span></span>
<span data-ttu-id="794bd-127">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="794bd-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="794bd-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="794bd-128">-Tag</span></span>
<span data-ttu-id="794bd-129">Címkék.</span><span class="sxs-lookup"><span data-stu-id="794bd-129">Tags.</span></span>

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

### <span data-ttu-id="794bd-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="794bd-130">-UserDefinedResource</span></span>
<span data-ttu-id="794bd-131">Felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="794bd-131">User defined resources.</span></span>

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

### <span data-ttu-id="794bd-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="794bd-132">-Confirm</span></span>
<span data-ttu-id="794bd-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="794bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794bd-134">-WhatIf</span></span>
<span data-ttu-id="794bd-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="794bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="794bd-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="794bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="794bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794bd-137">CommonParameters</span></span>
<span data-ttu-id="794bd-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="794bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794bd-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="794bd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794bd-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="794bd-140">INPUTS</span></span>

### <span data-ttu-id="794bd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="794bd-141">System.String</span></span>

### <span data-ttu-id="794bd-142">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="794bd-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="794bd-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="794bd-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="794bd-144">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="794bd-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="794bd-145">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="794bd-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="794bd-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="794bd-146">OUTPUTS</span></span>

### <span data-ttu-id="794bd-147">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="794bd-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="794bd-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="794bd-148">NOTES</span></span>

## <span data-ttu-id="794bd-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="794bd-149">RELATED LINKS</span></span>
