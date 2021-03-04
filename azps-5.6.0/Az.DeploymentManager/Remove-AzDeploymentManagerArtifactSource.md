---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: b10d73e118b590a06c2af5a1755a59d219f9f180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923673"
---
# <span data-ttu-id="766c8-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="766c8-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="766c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766c8-102">SYNOPSIS</span></span>
<span data-ttu-id="766c8-103">Törli a megadott összetevőforrást.</span><span class="sxs-lookup"><span data-stu-id="766c8-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="766c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="766c8-104">SYNTAX</span></span>

### <span data-ttu-id="766c8-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="766c8-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766c8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="766c8-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766c8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="766c8-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="766c8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="766c8-108">DESCRIPTION</span></span>
<span data-ttu-id="766c8-109">A **Remove-AzDeploymentManagerArtifactSource** parancsmag töröl egy olyan összetevőforrást, amely megadja az összetevő forrását a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="766c8-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="766c8-110">Másik módon meg is használhatja az ObjectSource objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="766c8-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="766c8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="766c8-111">EXAMPLES</span></span>

### <span data-ttu-id="766c8-112">1. példa: Az összetevő-forrás törlése</span><span class="sxs-lookup"><span data-stu-id="766c8-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="766c8-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="766c8-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="766c8-114">Ez a parancs törli a ContosoArtifactSource nevű összetevőforrást a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="766c8-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="766c8-115">2. példa: Objektumforrás törlése az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="766c8-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="766c8-116">Ez a parancs törli a ContosoArtifactSource nevű összetevőforrást a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="766c8-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="766c8-117">3. példa: Objektum használatával törölt objektumforrás</span><span class="sxs-lookup"><span data-stu-id="766c8-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="766c8-118">Ez a parancs törli azt az összetevőforrást, amelynek neve és ResourceGroup tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="766c8-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="766c8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766c8-119">PARAMETERS</span></span>

### <span data-ttu-id="766c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766c8-120">-DefaultProfile</span></span>
<span data-ttu-id="766c8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="766c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766c8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="766c8-122">-InputObject</span></span>
<span data-ttu-id="766c8-123">Az eltávolítható összetevő-forrás.</span><span class="sxs-lookup"><span data-stu-id="766c8-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="766c8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="766c8-124">-Name</span></span>
<span data-ttu-id="766c8-125">Az összetevő-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="766c8-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="766c8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="766c8-126">-PassThru</span></span>
<span data-ttu-id="766c8-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="766c8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="766c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="766c8-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="766c8-129">The resource group.</span></span>

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

### <span data-ttu-id="766c8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="766c8-130">-ResourceId</span></span>
<span data-ttu-id="766c8-131">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="766c8-131">The resource identifier.</span></span>

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

### <span data-ttu-id="766c8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="766c8-132">-Confirm</span></span>
<span data-ttu-id="766c8-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="766c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766c8-134">-WhatIf</span></span>
<span data-ttu-id="766c8-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="766c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="766c8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="766c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766c8-137">CommonParameters</span></span>
<span data-ttu-id="766c8-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766c8-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="766c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766c8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="766c8-140">INPUTS</span></span>

### <span data-ttu-id="766c8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="766c8-141">System.String</span></span>

### <span data-ttu-id="766c8-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="766c8-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="766c8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="766c8-143">OUTPUTS</span></span>

### <span data-ttu-id="766c8-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="766c8-144">System.Boolean</span></span>

## <span data-ttu-id="766c8-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="766c8-145">NOTES</span></span>

## <span data-ttu-id="766c8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="766c8-146">RELATED LINKS</span></span>
