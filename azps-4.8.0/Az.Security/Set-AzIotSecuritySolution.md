---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180891"
---
# <span data-ttu-id="47708-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47708-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="47708-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47708-102">SYNOPSIS</span></span>
<span data-ttu-id="47708-103">IoT biztonsági megoldás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="47708-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="47708-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47708-104">SYNTAX</span></span>

### <span data-ttu-id="47708-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47708-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47708-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="47708-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47708-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47708-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47708-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="47708-108">DESCRIPTION</span></span>
<span data-ttu-id="47708-109">Az Set-AzIotSecuritySolution parancsmag egy bizonyos IOT biztonsági megoldást hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="47708-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="47708-110">A IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt a IoT-eszközökről és a IoT hub-ról a fenyegetések megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="47708-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="47708-111">A IOT biztonsági megoldás nevének egyeznie kell a IOT-központ nevével.</span><span class="sxs-lookup"><span data-stu-id="47708-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="47708-112">Példák</span><span class="sxs-lookup"><span data-stu-id="47708-112">EXAMPLES</span></span>

### <span data-ttu-id="47708-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47708-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="47708-114">Új IOT biztonsági megoldás létrehozása "MySample" a IoT-hub esetén a "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" azonosítójú erőforrás-azonosítóval (az oldat nevének egyeznie kell a IoT-hub nevével)</span><span class="sxs-lookup"><span data-stu-id="47708-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="47708-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47708-115">PARAMETERS</span></span>

### <span data-ttu-id="47708-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47708-116">-DefaultProfile</span></span>
<span data-ttu-id="47708-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47708-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47708-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="47708-118">-DisabledDataSource</span></span>
<span data-ttu-id="47708-119">Le van tiltva az adatforrások.</span><span class="sxs-lookup"><span data-stu-id="47708-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47708-120">-DisplayName</span></span>
<span data-ttu-id="47708-121">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="47708-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-122">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="47708-122">-Enabled</span></span>
<span data-ttu-id="47708-123">Állapot.</span><span class="sxs-lookup"><span data-stu-id="47708-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-124">– Exportálás</span><span class="sxs-lookup"><span data-stu-id="47708-124">-Export</span></span>
<span data-ttu-id="47708-125">Az adatexportálás</span><span class="sxs-lookup"><span data-stu-id="47708-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47708-126">-InputObject</span></span>
<span data-ttu-id="47708-127">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="47708-127">Input Object.</span></span>

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

### <span data-ttu-id="47708-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="47708-128">-IotHub</span></span>
<span data-ttu-id="47708-129">IOT-hubok</span><span class="sxs-lookup"><span data-stu-id="47708-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="47708-130">-Location</span></span>
<span data-ttu-id="47708-131">Helyre.</span><span class="sxs-lookup"><span data-stu-id="47708-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47708-132">-Name</span></span>
<span data-ttu-id="47708-133">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="47708-133">Resource name.</span></span>

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

### <span data-ttu-id="47708-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="47708-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="47708-135">Javaslatok konfigurálása</span><span class="sxs-lookup"><span data-stu-id="47708-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="47708-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47708-136">-ResourceGroupName</span></span>
<span data-ttu-id="47708-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="47708-137">Resource group name.</span></span>

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

### <span data-ttu-id="47708-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47708-138">-ResourceId</span></span>
<span data-ttu-id="47708-139">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="47708-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="47708-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="47708-140">-Tag</span></span>
<span data-ttu-id="47708-141">Címkék.</span><span class="sxs-lookup"><span data-stu-id="47708-141">Tags.</span></span>

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

### <span data-ttu-id="47708-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="47708-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="47708-143">Maszk nélküli IP-naplózási állapot</span><span class="sxs-lookup"><span data-stu-id="47708-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="47708-144">-UserDefinedResource</span></span>
<span data-ttu-id="47708-145">Felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="47708-145">User defined resources.</span></span>

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

### <span data-ttu-id="47708-146">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="47708-146">-Workspace</span></span>
<span data-ttu-id="47708-147">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="47708-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47708-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47708-148">-Confirm</span></span>
<span data-ttu-id="47708-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47708-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47708-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47708-150">-WhatIf</span></span>
<span data-ttu-id="47708-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47708-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47708-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47708-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47708-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47708-153">CommonParameters</span></span>
<span data-ttu-id="47708-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47708-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47708-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47708-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47708-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47708-156">INPUTS</span></span>

### <span data-ttu-id="47708-157">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47708-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="47708-158">System. String</span><span class="sxs-lookup"><span data-stu-id="47708-158">System.String</span></span>

### <span data-ttu-id="47708-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47708-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47708-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="47708-160">System.String[]</span></span>

### <span data-ttu-id="47708-161">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="47708-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="47708-162">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="47708-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="47708-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47708-163">OUTPUTS</span></span>

### <span data-ttu-id="47708-164">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="47708-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="47708-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47708-165">NOTES</span></span>

## <span data-ttu-id="47708-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47708-166">RELATED LINKS</span></span>
