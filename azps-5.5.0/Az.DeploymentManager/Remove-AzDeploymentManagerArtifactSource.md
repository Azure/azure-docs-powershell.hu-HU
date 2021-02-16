---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153315"
---
# <span data-ttu-id="d3357-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d3357-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d3357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3357-102">SYNOPSIS</span></span>
<span data-ttu-id="d3357-103">Törli a megadott összetevőforrást.</span><span class="sxs-lookup"><span data-stu-id="d3357-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="d3357-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3357-104">SYNTAX</span></span>

### <span data-ttu-id="d3357-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3357-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3357-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3357-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3357-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d3357-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3357-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3357-108">DESCRIPTION</span></span>
<span data-ttu-id="d3357-109">A **Remove-AzDeploymentManagerArtifactSource** parancsmag töröl egy összetevőforrást, és megadja az összetevő forrását a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="d3357-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="d3357-110">Másik módon meg is használhatja az ObjectSource objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="d3357-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="d3357-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3357-111">EXAMPLES</span></span>

### <span data-ttu-id="d3357-112">1. példa: Az összetevő-forrás törlése</span><span class="sxs-lookup"><span data-stu-id="d3357-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="d3357-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d3357-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="d3357-114">Ez a parancs törli a ContosoArtifactSource nevű összetevőforrást a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="d3357-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d3357-115">2. példa: Objektumforrás törlése az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="d3357-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="d3357-116">Ez a parancs törli a ContosoArtifactSource nevű összetevőforrást a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="d3357-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d3357-117">3. példa: Objektum használatával törölt objektumforrás</span><span class="sxs-lookup"><span data-stu-id="d3357-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="d3357-118">Ez a parancs törli azt az összetevőforrást, amelynek neve és ResourceGroup tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="d3357-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="d3357-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3357-119">PARAMETERS</span></span>

### <span data-ttu-id="d3357-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3357-120">-DefaultProfile</span></span>
<span data-ttu-id="d3357-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3357-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3357-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3357-122">-InputObject</span></span>
<span data-ttu-id="d3357-123">Az eltávolítható összetevő-forrás.</span><span class="sxs-lookup"><span data-stu-id="d3357-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3357-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d3357-124">-Name</span></span>
<span data-ttu-id="d3357-125">Az összetevő-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="d3357-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3357-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3357-126">-PassThru</span></span>
<span data-ttu-id="d3357-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d3357-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d3357-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3357-128">-ResourceGroupName</span></span>
<span data-ttu-id="d3357-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="d3357-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3357-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3357-130">-ResourceId</span></span>
<span data-ttu-id="d3357-131">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d3357-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3357-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3357-132">-Confirm</span></span>
<span data-ttu-id="d3357-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3357-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3357-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3357-134">-WhatIf</span></span>
<span data-ttu-id="d3357-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3357-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3357-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3357-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3357-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3357-137">CommonParameters</span></span>
<span data-ttu-id="d3357-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3357-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3357-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3357-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3357-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3357-140">INPUTS</span></span>

### <span data-ttu-id="d3357-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d3357-141">System.String</span></span>

### <span data-ttu-id="d3357-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d3357-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d3357-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3357-143">OUTPUTS</span></span>

### <span data-ttu-id="d3357-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3357-144">System.Boolean</span></span>

## <span data-ttu-id="d3357-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3357-145">NOTES</span></span>

## <span data-ttu-id="d3357-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3357-146">RELATED LINKS</span></span>
