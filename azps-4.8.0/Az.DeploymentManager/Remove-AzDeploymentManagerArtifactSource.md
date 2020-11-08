---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017803"
---
# <span data-ttu-id="49a9e-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="49a9e-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="49a9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="49a9e-103">Törli a megadott tárgyi forrást.</span><span class="sxs-lookup"><span data-stu-id="49a9e-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="49a9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49a9e-104">SYNTAX</span></span>

### <span data-ttu-id="49a9e-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49a9e-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a9e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="49a9e-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a9e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="49a9e-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49a9e-108">DESCRIPTION</span></span>
<span data-ttu-id="49a9e-109">A **Remove-AzDeploymentManagerArtifactSource** parancsmag törli a tárgy forrását a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="49a9e-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="49a9e-110">Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="49a9e-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="49a9e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="49a9e-111">EXAMPLES</span></span>

### <span data-ttu-id="49a9e-112">Példa 1: tárgyi forrás törlése</span><span class="sxs-lookup"><span data-stu-id="49a9e-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="49a9e-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49a9e-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="49a9e-114">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="49a9e-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="49a9e-115">2. példa: tárgyi forrás törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="49a9e-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="49a9e-116">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="49a9e-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="49a9e-117">3. példa: tárgyi forrás törlése objektum használatával</span><span class="sxs-lookup"><span data-stu-id="49a9e-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="49a9e-118">Ez a parancs törli azt a tárgyi forrást, amelynek a neve és a ResourceGroup meg kell egyeznie az $artifactSourceObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="49a9e-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="49a9e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49a9e-119">PARAMETERS</span></span>

### <span data-ttu-id="49a9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a9e-120">-DefaultProfile</span></span>
<span data-ttu-id="49a9e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49a9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49a9e-122">-InputObject</span></span>
<span data-ttu-id="49a9e-123">Az eltávolítani kívánt tárgyi forrás.</span><span class="sxs-lookup"><span data-stu-id="49a9e-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="49a9e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49a9e-124">-Name</span></span>
<span data-ttu-id="49a9e-125">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="49a9e-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="49a9e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49a9e-126">-PassThru</span></span>
<span data-ttu-id="49a9e-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="49a9e-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="49a9e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a9e-128">-ResourceGroupName</span></span>
<span data-ttu-id="49a9e-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="49a9e-129">The resource group.</span></span>

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

### <span data-ttu-id="49a9e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49a9e-130">-ResourceId</span></span>
<span data-ttu-id="49a9e-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="49a9e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="49a9e-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49a9e-132">-Confirm</span></span>
<span data-ttu-id="49a9e-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49a9e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a9e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a9e-134">-WhatIf</span></span>
<span data-ttu-id="49a9e-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49a9e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a9e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49a9e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a9e-137">CommonParameters</span></span>
<span data-ttu-id="49a9e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49a9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a9e-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49a9e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a9e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a9e-140">INPUTS</span></span>

### <span data-ttu-id="49a9e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="49a9e-141">System.String</span></span>

### <span data-ttu-id="49a9e-142">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="49a9e-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="49a9e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a9e-143">OUTPUTS</span></span>

### <span data-ttu-id="49a9e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49a9e-144">System.Boolean</span></span>

## <span data-ttu-id="49a9e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49a9e-145">NOTES</span></span>

## <span data-ttu-id="49a9e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49a9e-146">RELATED LINKS</span></span>
