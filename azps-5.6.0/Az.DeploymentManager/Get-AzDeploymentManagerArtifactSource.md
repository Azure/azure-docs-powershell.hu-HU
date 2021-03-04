---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925801"
---
# <span data-ttu-id="acf92-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf92-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="acf92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf92-102">SYNOPSIS</span></span>

<span data-ttu-id="acf92-103">Beveszi az Összetevő forrást.</span><span class="sxs-lookup"><span data-stu-id="acf92-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="acf92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acf92-104">SYNTAX</span></span>

### <span data-ttu-id="acf92-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acf92-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acf92-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf92-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acf92-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="acf92-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf92-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acf92-108">DESCRIPTION</span></span>
<span data-ttu-id="acf92-109">A **Get-AzDeploymentManagerArtifactSource** parancsmag kap egy objektumforrást, és visszaad egy objektumot, amely az adott objektumforrást képviseli.</span><span class="sxs-lookup"><span data-stu-id="acf92-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="acf92-110">Adja meg az összetevőforrást a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="acf92-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="acf92-111">Másik módon meg is használhatja az ObjectSource objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="acf92-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="acf92-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acf92-112">EXAMPLES</span></span>

### <span data-ttu-id="acf92-113">1. példa: Összetevőforrás lekérte</span><span class="sxs-lookup"><span data-stu-id="acf92-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="acf92-114">Ez a parancs egy ContosoArtifactSource nevű összetevőforrást kap a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="acf92-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acf92-115">2. példa: Objektumforrás lekérte az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="acf92-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="acf92-116">Ez a parancs egy ContosoArtifactSource nevű összetevőforrást kap a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="acf92-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acf92-117">3. példa: Objektumforrás lekérte a New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf92-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="acf92-118">Ez a parancs egy olyan összetevőforrást kap, amelynek neve és ResourceGroup tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="acf92-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="acf92-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acf92-119">PARAMETERS</span></span>

### <span data-ttu-id="acf92-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf92-120">-DefaultProfile</span></span>
<span data-ttu-id="acf92-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acf92-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf92-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf92-122">-InputObject</span></span>
<span data-ttu-id="acf92-123">Object Source object.</span><span class="sxs-lookup"><span data-stu-id="acf92-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="acf92-124">-Name</span><span class="sxs-lookup"><span data-stu-id="acf92-124">-Name</span></span>
<span data-ttu-id="acf92-125">Az összetevő-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="acf92-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="acf92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf92-126">-ResourceGroupName</span></span>
<span data-ttu-id="acf92-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="acf92-127">The resource group.</span></span>

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

### <span data-ttu-id="acf92-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf92-128">-ResourceId</span></span>
<span data-ttu-id="acf92-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="acf92-129">The resource identifier.</span></span>

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

### <span data-ttu-id="acf92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf92-130">CommonParameters</span></span>
<span data-ttu-id="acf92-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf92-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acf92-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf92-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acf92-133">INPUTS</span></span>

### <span data-ttu-id="acf92-134">System.String</span><span class="sxs-lookup"><span data-stu-id="acf92-134">System.String</span></span>

### <span data-ttu-id="acf92-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf92-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="acf92-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf92-136">OUTPUTS</span></span>

### <span data-ttu-id="acf92-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="acf92-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="acf92-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acf92-138">NOTES</span></span>

## <span data-ttu-id="acf92-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acf92-139">RELATED LINKS</span></span>
