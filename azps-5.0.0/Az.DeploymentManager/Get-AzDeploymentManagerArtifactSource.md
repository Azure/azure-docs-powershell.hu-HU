---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297248"
---
# <span data-ttu-id="eb017-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="eb017-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="eb017-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb017-102">SYNOPSIS</span></span>

<span data-ttu-id="eb017-103">Megkapja az ereklyét forrást.</span><span class="sxs-lookup"><span data-stu-id="eb017-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="eb017-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb017-104">SYNTAX</span></span>

### <span data-ttu-id="eb017-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb017-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb017-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb017-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb017-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb017-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb017-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb017-108">DESCRIPTION</span></span>
<span data-ttu-id="eb017-109">A **Get-AzDeploymentManagerArtifactSource** parancsmag tárgyi forrást kap, és egy olyan objektumot ad eredményül, amely az adott tárgy forrását jelképezi.</span><span class="sxs-lookup"><span data-stu-id="eb017-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="eb017-110">Adja meg az tárgy forrását a neve és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="eb017-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="eb017-111">Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="eb017-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="eb017-112">Példák</span><span class="sxs-lookup"><span data-stu-id="eb017-112">EXAMPLES</span></span>

### <span data-ttu-id="eb017-113">Példa 1: tárgyi forrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="eb017-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="eb017-114">Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.</span><span class="sxs-lookup"><span data-stu-id="eb017-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eb017-115">2. példa: tárgyi forrás beszerzése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="eb017-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="eb017-116">Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.</span><span class="sxs-lookup"><span data-stu-id="eb017-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eb017-117">3. példa: tárgyi forrás beszerzése New-AzDeploymentManagerArtifactSource által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="eb017-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="eb017-118">Ez a parancs olyan tárgyi forrást kap, amelynek a neve és a ResourceGroup megegyezik a $artifactSourceObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="eb017-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="eb017-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb017-119">PARAMETERS</span></span>

### <span data-ttu-id="eb017-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb017-120">-DefaultProfile</span></span>
<span data-ttu-id="eb017-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb017-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb017-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb017-122">-InputObject</span></span>
<span data-ttu-id="eb017-123">Tárgy forrás objektum.</span><span class="sxs-lookup"><span data-stu-id="eb017-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="eb017-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb017-124">-Name</span></span>
<span data-ttu-id="eb017-125">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="eb017-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb017-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb017-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb017-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="eb017-127">The resource group.</span></span>

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

### <span data-ttu-id="eb017-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb017-128">-ResourceId</span></span>
<span data-ttu-id="eb017-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="eb017-129">The resource identifier.</span></span>

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

### <span data-ttu-id="eb017-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb017-130">CommonParameters</span></span>
<span data-ttu-id="eb017-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb017-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb017-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb017-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb017-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb017-133">INPUTS</span></span>

### <span data-ttu-id="eb017-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eb017-134">System.String</span></span>

### <span data-ttu-id="eb017-135">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="eb017-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="eb017-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb017-136">OUTPUTS</span></span>

### <span data-ttu-id="eb017-137">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="eb017-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="eb017-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb017-138">NOTES</span></span>

## <span data-ttu-id="eb017-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb017-139">RELATED LINKS</span></span>
