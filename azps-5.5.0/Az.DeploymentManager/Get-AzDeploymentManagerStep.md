---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163747"
---
# <span data-ttu-id="6db99-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6db99-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6db99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db99-102">SYNOPSIS</span></span>
<span data-ttu-id="6db99-103">Megkapja a lépést.</span><span class="sxs-lookup"><span data-stu-id="6db99-103">Gets the step.</span></span>

## <span data-ttu-id="6db99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6db99-104">SYNTAX</span></span>

### <span data-ttu-id="6db99-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6db99-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db99-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db99-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6db99-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6db99-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6db99-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6db99-108">DESCRIPTION</span></span>
<span data-ttu-id="6db99-109">A **Get-AzDeploymentManagerStep** parancsmag kap egy lépést, és visszaadja az adott lépésnek megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="6db99-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="6db99-110">Adja meg a lépést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="6db99-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="6db99-111">Másik lépésként meg is használhatja a Lépés objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="6db99-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="6db99-112">Ezt az objektumot helyben módosíthatja, majd a Set-AzDeploymentManagerStep parancsmag használatával módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="6db99-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="6db99-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6db99-113">EXAMPLES</span></span>

### <span data-ttu-id="6db99-114">1. példa: Lépés</span><span class="sxs-lookup"><span data-stu-id="6db99-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="6db99-115">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup-ban.</span><span class="sxs-lookup"><span data-stu-id="6db99-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6db99-116">2. példa: Lépés az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="6db99-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="6db99-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="6db99-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="6db99-118">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="6db99-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6db99-119">3. példa: Lépés lekérte a következő által visszaadott New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6db99-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="6db99-120">Ez a parancs egy olyan lépést kap, amelynek a neve és az Erőforráscsoport tulajdonsága megegyezik a $stepObject.</span><span class="sxs-lookup"><span data-stu-id="6db99-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="6db99-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6db99-121">PARAMETERS</span></span>

### <span data-ttu-id="6db99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db99-122">-DefaultProfile</span></span>
<span data-ttu-id="6db99-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6db99-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db99-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db99-124">-InputObject</span></span>
<span data-ttu-id="6db99-125">A lépés típusú erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="6db99-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db99-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6db99-126">-Name</span></span>
<span data-ttu-id="6db99-127">A lépés neve.</span><span class="sxs-lookup"><span data-stu-id="6db99-127">The name of the step.</span></span>

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

### <span data-ttu-id="6db99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db99-128">-ResourceGroupName</span></span>
<span data-ttu-id="6db99-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="6db99-129">The resource group.</span></span>

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

### <span data-ttu-id="6db99-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db99-130">-ResourceId</span></span>
<span data-ttu-id="6db99-131">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6db99-131">The resource identifier.</span></span>

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

### <span data-ttu-id="6db99-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db99-132">CommonParameters</span></span>
<span data-ttu-id="6db99-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db99-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db99-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6db99-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db99-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6db99-135">INPUTS</span></span>

### <span data-ttu-id="6db99-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6db99-136">System.String</span></span>

### <span data-ttu-id="6db99-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6db99-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6db99-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6db99-138">OUTPUTS</span></span>

### <span data-ttu-id="6db99-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6db99-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6db99-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6db99-140">NOTES</span></span>

## <span data-ttu-id="6db99-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6db99-141">RELATED LINKS</span></span>
