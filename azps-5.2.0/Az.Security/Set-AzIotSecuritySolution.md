---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335502"
---
# <span data-ttu-id="1d281-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1d281-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="1d281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d281-102">SYNOPSIS</span></span>
<span data-ttu-id="1d281-103">IoT-biztonsági megoldás létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="1d281-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="1d281-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d281-104">SYNTAX</span></span>

### <span data-ttu-id="1d281-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d281-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d281-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1d281-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d281-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d281-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d281-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d281-108">DESCRIPTION</span></span>
<span data-ttu-id="1d281-109">A Set-AzIotSecuritySolution parancsmag létrehoz vagy frissítéseket hoz létre egy adott iot biztonsági megoldással.</span><span class="sxs-lookup"><span data-stu-id="1d281-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="1d281-110">Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="1d281-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="1d281-111">Az iot biztonsági megoldás nevének meg kell egyeznie az iot-központ nevével.</span><span class="sxs-lookup"><span data-stu-id="1d281-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="1d281-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d281-112">EXAMPLES</span></span>

### <span data-ttu-id="1d281-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="1d281-113">Example 1</span></span>
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

<span data-ttu-id="1d281-114">Hozzon létre új iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (a megoldás nevének meg kell egyeznie az IoT-központ nevével)</span><span class="sxs-lookup"><span data-stu-id="1d281-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="1d281-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d281-115">PARAMETERS</span></span>

### <span data-ttu-id="1d281-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d281-116">-DefaultProfile</span></span>
<span data-ttu-id="1d281-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d281-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d281-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="1d281-118">-DisabledDataSource</span></span>
<span data-ttu-id="1d281-119">Letiltott adatforrások.</span><span class="sxs-lookup"><span data-stu-id="1d281-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="1d281-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d281-120">-DisplayName</span></span>
<span data-ttu-id="1d281-121">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="1d281-121">Display name.</span></span>

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

### <span data-ttu-id="1d281-122">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="1d281-122">-Enabled</span></span>
<span data-ttu-id="1d281-123">Állapot.</span><span class="sxs-lookup"><span data-stu-id="1d281-123">Status .</span></span>

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

### <span data-ttu-id="1d281-124">-Export</span><span class="sxs-lookup"><span data-stu-id="1d281-124">-Export</span></span>
<span data-ttu-id="1d281-125">Adatok exportálása</span><span class="sxs-lookup"><span data-stu-id="1d281-125">Export data.</span></span>

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

### <span data-ttu-id="1d281-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d281-126">-InputObject</span></span>
<span data-ttu-id="1d281-127">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="1d281-127">Input Object.</span></span>

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

### <span data-ttu-id="1d281-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="1d281-128">-IotHub</span></span>
<span data-ttu-id="1d281-129">Iot hubok.</span><span class="sxs-lookup"><span data-stu-id="1d281-129">Iot hubs.</span></span>

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

### <span data-ttu-id="1d281-130">-Location</span><span class="sxs-lookup"><span data-stu-id="1d281-130">-Location</span></span>
<span data-ttu-id="1d281-131">Hely.</span><span class="sxs-lookup"><span data-stu-id="1d281-131">Location.</span></span>

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

### <span data-ttu-id="1d281-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1d281-132">-Name</span></span>
<span data-ttu-id="1d281-133">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1d281-133">Resource name.</span></span>

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

### <span data-ttu-id="1d281-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d281-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="1d281-135">Javaslatok konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="1d281-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="1d281-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d281-136">-ResourceGroupName</span></span>
<span data-ttu-id="1d281-137">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d281-137">Resource group name.</span></span>

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

### <span data-ttu-id="1d281-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d281-138">-ResourceId</span></span>
<span data-ttu-id="1d281-139">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="1d281-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1d281-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d281-140">-Tag</span></span>
<span data-ttu-id="1d281-141">Címkék.</span><span class="sxs-lookup"><span data-stu-id="1d281-141">Tags.</span></span>

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

### <span data-ttu-id="1d281-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="1d281-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="1d281-143">A be nem ékeletlen IP-naplózás állapota.</span><span class="sxs-lookup"><span data-stu-id="1d281-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="1d281-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="1d281-144">-UserDefinedResource</span></span>
<span data-ttu-id="1d281-145">Felhasználó által definiált erőforrások.</span><span class="sxs-lookup"><span data-stu-id="1d281-145">User defined resources.</span></span>

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

### <span data-ttu-id="1d281-146">-Workspace</span><span class="sxs-lookup"><span data-stu-id="1d281-146">-Workspace</span></span>
<span data-ttu-id="1d281-147">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1d281-147">Workspace ID.</span></span>

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

### <span data-ttu-id="1d281-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d281-148">-Confirm</span></span>
<span data-ttu-id="1d281-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d281-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d281-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d281-150">-WhatIf</span></span>
<span data-ttu-id="1d281-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d281-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d281-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d281-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d281-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d281-153">CommonParameters</span></span>
<span data-ttu-id="1d281-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d281-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d281-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d281-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d281-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d281-156">INPUTS</span></span>

### <span data-ttu-id="1d281-157">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1d281-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="1d281-158">System.String</span><span class="sxs-lookup"><span data-stu-id="1d281-158">System.String</span></span>

### <span data-ttu-id="1d281-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d281-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1d281-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1d281-160">System.String[]</span></span>

### <span data-ttu-id="1d281-161">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="1d281-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="1d281-162">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="1d281-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="1d281-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d281-163">OUTPUTS</span></span>

### <span data-ttu-id="1d281-164">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1d281-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="1d281-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d281-165">NOTES</span></span>

## <span data-ttu-id="1d281-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d281-166">RELATED LINKS</span></span>
