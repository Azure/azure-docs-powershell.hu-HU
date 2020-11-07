---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671782"
---
# <span data-ttu-id="acf24-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="acf24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acf24-102">SYNOPSIS</span></span>
<span data-ttu-id="acf24-103">Egy tárgy forrását kapja.</span><span class="sxs-lookup"><span data-stu-id="acf24-103">Gets an artifact source.</span></span>

## <span data-ttu-id="acf24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acf24-104">SYNTAX</span></span>

### <span data-ttu-id="acf24-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acf24-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acf24-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf24-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acf24-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="acf24-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf24-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="acf24-108">DESCRIPTION</span></span>
<span data-ttu-id="acf24-109">A **Get-AzureRmDeploymentManagerArtifactSource** parancsmag tárgyi forrást kap, és egy olyan objektumot ad eredményül, amely az adott tárgy forrását jelképezi.</span><span class="sxs-lookup"><span data-stu-id="acf24-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="acf24-110">Adja meg az tárgy forrását a neve és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="acf24-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="acf24-111">Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="acf24-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="acf24-112">Ezt az objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerArtifactSource parancsmag használatával alkalmazhatja az objektumon végzett módosításokat.</span><span class="sxs-lookup"><span data-stu-id="acf24-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="acf24-113">Példák</span><span class="sxs-lookup"><span data-stu-id="acf24-113">EXAMPLES</span></span>

### <span data-ttu-id="acf24-114">Példa 1: tárgyi forrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="acf24-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="acf24-115">Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.</span><span class="sxs-lookup"><span data-stu-id="acf24-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acf24-116">2. példa: tárgyi forrás beszerzése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="acf24-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="acf24-117">Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.</span><span class="sxs-lookup"><span data-stu-id="acf24-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acf24-118">3. példa: tárgyi forrás beszerzése New-AzureRmDeploymentManagerArtifactSource által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="acf24-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="acf24-119">Ez a parancs olyan tárgyi forrást kap, amelynek a neve és a ResourceGroup megegyezik a $artifactSourceObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="acf24-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="acf24-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acf24-120">PARAMETERS</span></span>

### <span data-ttu-id="acf24-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-121">-ArtifactSource</span></span>
<span data-ttu-id="acf24-122">Tárgy forrás objektum.</span><span class="sxs-lookup"><span data-stu-id="acf24-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="acf24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf24-123">-DefaultProfile</span></span>
<span data-ttu-id="acf24-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acf24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf24-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acf24-125">-Name</span></span>
<span data-ttu-id="acf24-126">A tárgy forrásának neve.</span><span class="sxs-lookup"><span data-stu-id="acf24-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="acf24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf24-127">-ResourceGroupName</span></span>
<span data-ttu-id="acf24-128">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="acf24-128">The resource group.</span></span>

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

### <span data-ttu-id="acf24-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf24-129">-ResourceId</span></span>
<span data-ttu-id="acf24-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="acf24-130">The resource identifier.</span></span>

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

### <span data-ttu-id="acf24-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf24-131">CommonParameters</span></span>
<span data-ttu-id="acf24-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acf24-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf24-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf24-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf24-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf24-134">INPUTS</span></span>

### <span data-ttu-id="acf24-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="acf24-135">None</span></span>

## <span data-ttu-id="acf24-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf24-136">OUTPUTS</span></span>

### <span data-ttu-id="acf24-137">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="acf24-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acf24-138">NOTES</span></span>

## <span data-ttu-id="acf24-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acf24-139">RELATED LINKS</span></span>

[<span data-ttu-id="acf24-140">Új – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="acf24-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="acf24-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf24-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)