---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 1977fca9843c00d80d398a1dcd0bb967883cb5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666652"
---
# <span data-ttu-id="166a0-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="166a0-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="166a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="166a0-102">SYNOPSIS</span></span>
<span data-ttu-id="166a0-103">Törli a megadott tárgyi forrást.</span><span class="sxs-lookup"><span data-stu-id="166a0-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="166a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="166a0-104">SYNTAX</span></span>

### <span data-ttu-id="166a0-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="166a0-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166a0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="166a0-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166a0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="166a0-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166a0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="166a0-108">DESCRIPTION</span></span>
<span data-ttu-id="166a0-109">A **Remove-AzDeploymentManagerArtifactSource** parancsmag törli a tárgy forrását a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="166a0-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="166a0-110">Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="166a0-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="166a0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="166a0-111">EXAMPLES</span></span>

### <span data-ttu-id="166a0-112">Példa 1: tárgyi forrás törlése</span><span class="sxs-lookup"><span data-stu-id="166a0-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="166a0-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="166a0-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="166a0-114">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="166a0-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="166a0-115">2. példa: tárgyi forrás törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="166a0-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="166a0-116">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="166a0-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="166a0-117">3. példa: tárgyi forrás törlése objektum használatával</span><span class="sxs-lookup"><span data-stu-id="166a0-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="166a0-118">Ez a parancs törli azt a tárgyi forrást, amelynek a neve és a ResourceGroup meg kell egyeznie az $artifactSourceObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="166a0-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="166a0-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="166a0-119">PARAMETERS</span></span>

### <span data-ttu-id="166a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166a0-120">-DefaultProfile</span></span>
<span data-ttu-id="166a0-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="166a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166a0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="166a0-122">-InputObject</span></span>
<span data-ttu-id="166a0-123">Az eltávolítani kívánt tárgyi forrás.</span><span class="sxs-lookup"><span data-stu-id="166a0-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="166a0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="166a0-124">-Name</span></span>
<span data-ttu-id="166a0-125">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="166a0-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="166a0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="166a0-126">-PassThru</span></span>
<span data-ttu-id="166a0-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="166a0-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="166a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="166a0-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="166a0-129">The resource group.</span></span>

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

### <span data-ttu-id="166a0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="166a0-130">-ResourceId</span></span>
<span data-ttu-id="166a0-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="166a0-131">The resource identifier.</span></span>

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

### <span data-ttu-id="166a0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="166a0-132">-Confirm</span></span>
<span data-ttu-id="166a0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="166a0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166a0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166a0-134">-WhatIf</span></span>
<span data-ttu-id="166a0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="166a0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="166a0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="166a0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="166a0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166a0-137">CommonParameters</span></span>
<span data-ttu-id="166a0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="166a0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166a0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166a0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166a0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="166a0-140">INPUTS</span></span>

### <span data-ttu-id="166a0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="166a0-141">System.String</span></span>

### <span data-ttu-id="166a0-142">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="166a0-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="166a0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="166a0-143">OUTPUTS</span></span>

### <span data-ttu-id="166a0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="166a0-144">System.Boolean</span></span>

## <span data-ttu-id="166a0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="166a0-145">NOTES</span></span>

## <span data-ttu-id="166a0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="166a0-146">RELATED LINKS</span></span>
