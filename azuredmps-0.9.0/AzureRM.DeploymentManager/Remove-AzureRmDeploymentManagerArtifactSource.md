---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490848"
---
# <span data-ttu-id="d9967-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d9967-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9967-102">SYNOPSIS</span></span>
<span data-ttu-id="d9967-103">Tárgyi forrás törlése</span><span class="sxs-lookup"><span data-stu-id="d9967-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="d9967-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9967-104">SYNTAX</span></span>

### <span data-ttu-id="d9967-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9967-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9967-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9967-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9967-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9967-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9967-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9967-108">DESCRIPTION</span></span>
<span data-ttu-id="d9967-109">A **Remove-AzureRmDeploymentManagerArtifactSource** parancsmag törli a tárgy forrását a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="d9967-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="d9967-110">Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d9967-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="d9967-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d9967-111">EXAMPLES</span></span>

### <span data-ttu-id="d9967-112">Példa 1: tárgyi forrás törlése</span><span class="sxs-lookup"><span data-stu-id="d9967-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="d9967-113">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d9967-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d9967-114">2. példa: tárgyi forrás törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="d9967-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="d9967-115">Ez a parancs törli a ContosoArtifactSource nevű tárgyi forrást a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d9967-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d9967-116">3. példa: tárgyi forrás törlése objektum használatával</span><span class="sxs-lookup"><span data-stu-id="d9967-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="d9967-117">Ez a parancs törli azt a tárgyi forrást, amelynek a neve és a ResourceGroup meg kell egyeznie az $artifactSourceObject nevével és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="d9967-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="d9967-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9967-118">PARAMETERS</span></span>

### <span data-ttu-id="d9967-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-119">-ArtifactSource</span></span>
<span data-ttu-id="d9967-120">A megszüntetni kívánt tárgy-tároló.</span><span class="sxs-lookup"><span data-stu-id="d9967-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="d9967-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9967-121">-DefaultProfile</span></span>
<span data-ttu-id="d9967-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9967-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9967-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d9967-123">-Force</span></span>
<span data-ttu-id="d9967-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9967-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d9967-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9967-125">-Name</span></span>
<span data-ttu-id="d9967-126">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="d9967-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9967-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9967-127">-PassThru</span></span>
<span data-ttu-id="d9967-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d9967-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d9967-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9967-129">-ResourceGroupName</span></span>
<span data-ttu-id="d9967-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="d9967-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9967-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9967-131">-ResourceId</span></span>
<span data-ttu-id="d9967-132">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d9967-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d9967-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9967-133">-Confirm</span></span>
<span data-ttu-id="d9967-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9967-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9967-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9967-135">-WhatIf</span></span>
<span data-ttu-id="d9967-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9967-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9967-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9967-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9967-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9967-138">CommonParameters</span></span>
<span data-ttu-id="d9967-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9967-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9967-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9967-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9967-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9967-141">INPUTS</span></span>

### <span data-ttu-id="d9967-142">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d9967-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9967-143">OUTPUTS</span></span>

### <span data-ttu-id="d9967-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9967-144">System.Boolean</span></span>

## <span data-ttu-id="d9967-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9967-145">NOTES</span></span>

## <span data-ttu-id="d9967-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9967-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9967-147">Új – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="d9967-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="d9967-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d9967-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)