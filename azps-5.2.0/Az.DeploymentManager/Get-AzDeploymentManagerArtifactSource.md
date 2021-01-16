---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355962"
---
# <span data-ttu-id="6dabd-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6dabd-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="6dabd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dabd-102">SYNOPSIS</span></span>

<span data-ttu-id="6dabd-103">Beveszi az Összetevő forrást.</span><span class="sxs-lookup"><span data-stu-id="6dabd-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="6dabd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6dabd-104">SYNTAX</span></span>

### <span data-ttu-id="6dabd-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6dabd-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dabd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dabd-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dabd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6dabd-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dabd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6dabd-108">DESCRIPTION</span></span>
<span data-ttu-id="6dabd-109">A **Get-AzDeploymentManagerArtifactSource** parancsmag kap egy objektumforrást, és visszaad egy objektumot, amely az adott objektumforrást képviseli.</span><span class="sxs-lookup"><span data-stu-id="6dabd-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="6dabd-110">Adja meg az összetevőforrást a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="6dabd-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="6dabd-111">Másik módon meg is használhatja az ObjectSource objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="6dabd-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="6dabd-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6dabd-112">EXAMPLES</span></span>

### <span data-ttu-id="6dabd-113">1. példa: Összetevőforrás lekérte</span><span class="sxs-lookup"><span data-stu-id="6dabd-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="6dabd-114">Ez a parancs egy ContosoArtifactSource nevű összetevőforrást kap a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="6dabd-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dabd-115">2. példa: Objektumforrás lekérte az erőforrás-azonosítót használva</span><span class="sxs-lookup"><span data-stu-id="6dabd-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="6dabd-116">Ez a parancs egy ContosoArtifactSource nevű összetevőforrást kap a ContosoResourceGroupban.</span><span class="sxs-lookup"><span data-stu-id="6dabd-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dabd-117">3. példa: Objektumforrás lekérte a New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6dabd-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="6dabd-118">Ez a parancs egy olyan összetevőforrást kap, amelynek neve és ResourceGroup tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="6dabd-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="6dabd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dabd-119">PARAMETERS</span></span>

### <span data-ttu-id="6dabd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dabd-120">-DefaultProfile</span></span>
<span data-ttu-id="6dabd-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6dabd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dabd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dabd-122">-InputObject</span></span>
<span data-ttu-id="6dabd-123">Object Source object.</span><span class="sxs-lookup"><span data-stu-id="6dabd-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="6dabd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6dabd-124">-Name</span></span>
<span data-ttu-id="6dabd-125">Az összetevő-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="6dabd-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="6dabd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dabd-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dabd-127">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="6dabd-127">The resource group.</span></span>

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

### <span data-ttu-id="6dabd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dabd-128">-ResourceId</span></span>
<span data-ttu-id="6dabd-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6dabd-129">The resource identifier.</span></span>

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

### <span data-ttu-id="6dabd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dabd-130">CommonParameters</span></span>
<span data-ttu-id="6dabd-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dabd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dabd-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dabd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dabd-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dabd-133">INPUTS</span></span>

### <span data-ttu-id="6dabd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6dabd-134">System.String</span></span>

### <span data-ttu-id="6dabd-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6dabd-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6dabd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6dabd-136">OUTPUTS</span></span>

### <span data-ttu-id="6dabd-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6dabd-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6dabd-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6dabd-138">NOTES</span></span>

## <span data-ttu-id="6dabd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6dabd-139">RELATED LINKS</span></span>
