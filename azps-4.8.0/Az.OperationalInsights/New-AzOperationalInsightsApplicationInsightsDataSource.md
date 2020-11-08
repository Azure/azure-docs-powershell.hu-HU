---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024512"
---
# <span data-ttu-id="3bc7b-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc7b-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="3bc7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc7b-103">Naplók gyűjtése az adott Application-Insights alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="3bc7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bc7b-104">SYNTAX</span></span>

### <span data-ttu-id="3bc7b-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bc7b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc7b-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="3bc7b-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc7b-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc7b-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc7b-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="3bc7b-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc7b-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc7b-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bc7b-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bc7b-110">DESCRIPTION</span></span>
<span data-ttu-id="3bc7b-111">A **New-AzOperationalInsightsApplicationInsightsDataSource** parancsmag lehetővé teszi a naplók gyűjteményét egy adott Application-Insights alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="3bc7b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3bc7b-112">EXAMPLES</span></span>

### <span data-ttu-id="3bc7b-113">1. példa: alkalmazás-betekintési adatforrás létrehozása a munkaterületen</span><span class="sxs-lookup"><span data-stu-id="3bc7b-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="3bc7b-114">Ez a parancs létrehoz egy, az adott alkalmazáshoz tartozó alkalmazás-adatforrást egy adott alkalmazásban egy adott naplózási Analytics-munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="3bc7b-115">Ez lehetővé teszi, hogy az adott alkalmazásból származó naplók gyűjtése a log Analytics-munkaterületre történjen.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="3bc7b-116">2. példa: a munkaterület-objektum beolvasása és az alkalmazás létrehozása – adatforrások létrehozása az alkalmazás erőforrás-azonosítója szerint</span><span class="sxs-lookup"><span data-stu-id="3bc7b-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="3bc7b-117">Ez a parancs bemutatja a log Analytics Workspace-objektum beszerzését, majd a kimenet átadásával létrehoz egy kapcsolódó alkalmazás-adatforrást az alkalmazás erőforrás-azonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="3bc7b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bc7b-118">PARAMETERS</span></span>

### <span data-ttu-id="3bc7b-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="3bc7b-119">-ApplicationName</span></span>
<span data-ttu-id="3bc7b-120">A kapcsolt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc7b-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="3bc7b-122">A kapcsolt alkalmazás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc7b-123">-ApplicationResourceId</span></span>
<span data-ttu-id="3bc7b-124">A kapcsolt alkalmazás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bc7b-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="3bc7b-126">A kapcsolt alkalmazás előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc7b-127">-DefaultProfile</span></span>
<span data-ttu-id="3bc7b-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc7b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="3bc7b-129">-Force</span></span>
<span data-ttu-id="3bc7b-130">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3bc7b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc7b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3bc7b-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-133">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="3bc7b-133">-Workspace</span></span>
<span data-ttu-id="3bc7b-134">Az adatforrást tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bc7b-135">-WorkspaceName</span></span>
<span data-ttu-id="3bc7b-136">Annak a munkaterületnek a neve, amely az adatforrást fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc7b-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bc7b-137">-Confirm</span></span>
<span data-ttu-id="3bc7b-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc7b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc7b-139">-WhatIf</span></span>
<span data-ttu-id="3bc7b-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc7b-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bc7b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc7b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc7b-142">CommonParameters</span></span>
<span data-ttu-id="3bc7b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bc7b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc7b-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc7b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc7b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc7b-145">INPUTS</span></span>

### <span data-ttu-id="3bc7b-146">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3bc7b-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3bc7b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc7b-147">System.String</span></span>

## <span data-ttu-id="3bc7b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc7b-148">OUTPUTS</span></span>

### <span data-ttu-id="3bc7b-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3bc7b-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3bc7b-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bc7b-150">NOTES</span></span>

## <span data-ttu-id="3bc7b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bc7b-151">RELATED LINKS</span></span>
