---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014387"
---
# <span data-ttu-id="c34fe-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c34fe-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="c34fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c34fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c34fe-103">Megkapja a lépést.</span><span class="sxs-lookup"><span data-stu-id="c34fe-103">Gets the step.</span></span>

## <span data-ttu-id="c34fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c34fe-104">SYNTAX</span></span>

### <span data-ttu-id="c34fe-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c34fe-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c34fe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c34fe-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c34fe-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c34fe-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c34fe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c34fe-108">DESCRIPTION</span></span>
<span data-ttu-id="c34fe-109">A **Get-AzDeploymentManagerStep** parancsmag lépésről lépésre lép, és egy olyan objektumot ad eredményül, amely a lépést jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c34fe-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="c34fe-110">Adja meg a lépést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c34fe-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="c34fe-111">Másik lehetőségként a Step objektum vagy a ResourceId is megadható.</span><span class="sxs-lookup"><span data-stu-id="c34fe-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="c34fe-112">Ezt az objektumot helyileg módosíthatja, majd a Set-AzDeploymentManagerStep parancsmag használatával alkalmazhatja az objektumon végzett módosításokat.</span><span class="sxs-lookup"><span data-stu-id="c34fe-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="c34fe-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c34fe-113">EXAMPLES</span></span>

### <span data-ttu-id="c34fe-114">Példa 1: lépés kérése</span><span class="sxs-lookup"><span data-stu-id="c34fe-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="c34fe-115">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c34fe-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c34fe-116">2. példa: lépés kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c34fe-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="c34fe-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c34fe-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="c34fe-118">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c34fe-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c34fe-119">3. példa: lépés beszerzése New-AzDeploymentManagerStep által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="c34fe-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="c34fe-120">Ez a parancs olyan lépésekkel lép be, amelyeknek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="c34fe-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="c34fe-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c34fe-121">PARAMETERS</span></span>

### <span data-ttu-id="c34fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34fe-122">-DefaultProfile</span></span>
<span data-ttu-id="c34fe-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c34fe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c34fe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c34fe-124">-InputObject</span></span>
<span data-ttu-id="c34fe-125">A lépés erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="c34fe-125">The step resource object.</span></span>

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

### <span data-ttu-id="c34fe-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c34fe-126">-Name</span></span>
<span data-ttu-id="c34fe-127">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c34fe-127">The name of the step.</span></span>

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

### <span data-ttu-id="c34fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="c34fe-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="c34fe-129">The resource group.</span></span>

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

### <span data-ttu-id="c34fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c34fe-130">-ResourceId</span></span>
<span data-ttu-id="c34fe-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c34fe-131">The resource identifier.</span></span>

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

### <span data-ttu-id="c34fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34fe-132">CommonParameters</span></span>
<span data-ttu-id="c34fe-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c34fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34fe-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c34fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34fe-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c34fe-135">INPUTS</span></span>

### <span data-ttu-id="c34fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c34fe-136">System.String</span></span>

### <span data-ttu-id="c34fe-137">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c34fe-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c34fe-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c34fe-138">OUTPUTS</span></span>

### <span data-ttu-id="c34fe-139">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c34fe-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c34fe-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c34fe-140">NOTES</span></span>

## <span data-ttu-id="c34fe-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c34fe-141">RELATED LINKS</span></span>
