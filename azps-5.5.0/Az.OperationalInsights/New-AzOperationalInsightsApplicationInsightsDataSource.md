---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206351"
---
# <span data-ttu-id="94449-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="94449-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="94449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94449-102">SYNOPSIS</span></span>
<span data-ttu-id="94449-103">Naplókat gyűjt az adott Application-Insights alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="94449-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="94449-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94449-104">SYNTAX</span></span>

### <span data-ttu-id="94449-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94449-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94449-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="94449-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94449-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="94449-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94449-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="94449-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94449-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="94449-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94449-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94449-110">DESCRIPTION</span></span>
<span data-ttu-id="94449-111">A **New-AzOperationalInsightsApplicationInsightsDataSource** parancsmag lehetővé teszi a naplók egy adott Application-Insights gyűjtését.</span><span class="sxs-lookup"><span data-stu-id="94449-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="94449-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94449-112">EXAMPLES</span></span>

### <span data-ttu-id="94449-113">1. példa: Alkalmazásstatikációk adatforrásának létrehozása a munkaterületen</span><span class="sxs-lookup"><span data-stu-id="94449-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="94449-114">Ez a parancs egy adott alkalmazás alkalmazás-insights adatforrását hozza létre egy adott naplóelemzési munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="94449-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="94449-115">Ez lehetővé teszi a naplók gyűjteményét az adott alkalmazásból a naplóelemzés munkaterületére.</span><span class="sxs-lookup"><span data-stu-id="94449-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="94449-116">2. példa: Munkaterület-objektum lekérte és alkalmazás-insights adatforrás létrehozása az alkalmazáserőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="94449-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="94449-117">Ez a parancs azt mutatja be, hogy hogyan juthat hozzá egy log analytics munkaterületi objektumhoz, majd a kimenetet átküldve létrehoz egy kapcsolódó alkalmazás-insights adatforrást az alkalmazáserőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="94449-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="94449-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94449-118">PARAMETERS</span></span>

### <span data-ttu-id="94449-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="94449-119">-ApplicationName</span></span>
<span data-ttu-id="94449-120">A csatolt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="94449-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="94449-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94449-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="94449-122">A csatolt alkalmazás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="94449-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="94449-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="94449-123">-ApplicationResourceId</span></span>
<span data-ttu-id="94449-124">A csatolt alkalmazáserőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94449-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="94449-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94449-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="94449-126">A csatolt alkalmazás előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="94449-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="94449-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94449-127">-DefaultProfile</span></span>
<span data-ttu-id="94449-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94449-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94449-129">-Force</span><span class="sxs-lookup"><span data-stu-id="94449-129">-Force</span></span>
<span data-ttu-id="94449-130">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94449-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="94449-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94449-131">-ResourceGroupName</span></span>
<span data-ttu-id="94449-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94449-132">The resource group name.</span></span>

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

### <span data-ttu-id="94449-133">-Workspace</span><span class="sxs-lookup"><span data-stu-id="94449-133">-Workspace</span></span>
<span data-ttu-id="94449-134">Az adatforrást tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="94449-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="94449-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94449-135">-WorkspaceName</span></span>
<span data-ttu-id="94449-136">Az adatforrást tartalmazó munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="94449-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="94449-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94449-137">-Confirm</span></span>
<span data-ttu-id="94449-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94449-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94449-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94449-139">-WhatIf</span></span>
<span data-ttu-id="94449-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94449-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94449-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94449-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94449-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94449-142">CommonParameters</span></span>
<span data-ttu-id="94449-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94449-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94449-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94449-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94449-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94449-145">INPUTS</span></span>

### <span data-ttu-id="94449-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="94449-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="94449-147">System.String</span><span class="sxs-lookup"><span data-stu-id="94449-147">System.String</span></span>

## <span data-ttu-id="94449-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94449-148">OUTPUTS</span></span>

### <span data-ttu-id="94449-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="94449-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="94449-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94449-150">NOTES</span></span>

## <span data-ttu-id="94449-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94449-151">RELATED LINKS</span></span>
