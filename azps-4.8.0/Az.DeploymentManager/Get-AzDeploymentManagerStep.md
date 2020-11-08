---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182283"
---
# <span data-ttu-id="f4e56-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f4e56-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f4e56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4e56-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e56-103">Megkapja a lépést.</span><span class="sxs-lookup"><span data-stu-id="f4e56-103">Gets the step.</span></span>

## <span data-ttu-id="f4e56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4e56-104">SYNTAX</span></span>

### <span data-ttu-id="f4e56-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4e56-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e56-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e56-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4e56-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4e56-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4e56-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4e56-108">DESCRIPTION</span></span>
<span data-ttu-id="f4e56-109">A **Get-AzDeploymentManagerStep** parancsmag lépésről lépésre lép, és egy olyan objektumot ad eredményül, amely a lépést jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f4e56-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="f4e56-110">Adja meg a lépést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f4e56-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="f4e56-111">Másik lehetőségként a Step objektum vagy a ResourceId is megadható.</span><span class="sxs-lookup"><span data-stu-id="f4e56-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="f4e56-112">Ezt az objektumot helyileg módosíthatja, majd a Set-AzDeploymentManagerStep parancsmag használatával alkalmazhatja az objektumon végzett módosításokat.</span><span class="sxs-lookup"><span data-stu-id="f4e56-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f4e56-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f4e56-113">EXAMPLES</span></span>

### <span data-ttu-id="f4e56-114">Példa 1: lépés kérése</span><span class="sxs-lookup"><span data-stu-id="f4e56-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="f4e56-115">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f4e56-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4e56-116">2. példa: lépés kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f4e56-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="f4e56-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4e56-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="f4e56-118">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f4e56-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4e56-119">3. példa: lépés beszerzése New-AzDeploymentManagerStep által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="f4e56-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="f4e56-120">Ez a parancs olyan lépésekkel lép be, amelyeknek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="f4e56-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="f4e56-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4e56-121">PARAMETERS</span></span>

### <span data-ttu-id="f4e56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e56-122">-DefaultProfile</span></span>
<span data-ttu-id="f4e56-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4e56-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e56-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4e56-124">-InputObject</span></span>
<span data-ttu-id="f4e56-125">A lépés erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="f4e56-125">The step resource object.</span></span>

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

### <span data-ttu-id="f4e56-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4e56-126">-Name</span></span>
<span data-ttu-id="f4e56-127">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f4e56-127">The name of the step.</span></span>

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

### <span data-ttu-id="f4e56-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e56-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4e56-129">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="f4e56-129">The resource group.</span></span>

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

### <span data-ttu-id="f4e56-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e56-130">-ResourceId</span></span>
<span data-ttu-id="f4e56-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f4e56-131">The resource identifier.</span></span>

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

### <span data-ttu-id="f4e56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e56-132">CommonParameters</span></span>
<span data-ttu-id="f4e56-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4e56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e56-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4e56-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e56-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e56-135">INPUTS</span></span>

### <span data-ttu-id="f4e56-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e56-136">System.String</span></span>

### <span data-ttu-id="f4e56-137">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f4e56-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f4e56-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e56-138">OUTPUTS</span></span>

### <span data-ttu-id="f4e56-139">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f4e56-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f4e56-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4e56-140">NOTES</span></span>

## <span data-ttu-id="f4e56-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4e56-141">RELATED LINKS</span></span>
