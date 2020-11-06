---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490951"
---
# <span data-ttu-id="42a71-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="42a71-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="42a71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42a71-102">SYNOPSIS</span></span>
<span data-ttu-id="42a71-103">A központi telepítő lépés beolvasása</span><span class="sxs-lookup"><span data-stu-id="42a71-103">Gets the deployment step.</span></span>

## <span data-ttu-id="42a71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42a71-104">SYNTAX</span></span>

### <span data-ttu-id="42a71-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42a71-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42a71-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a71-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42a71-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="42a71-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42a71-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42a71-108">DESCRIPTION</span></span>
<span data-ttu-id="42a71-109">A **Get-AzureRmDeploymentManagerStep** parancsmag lépésről lépésre lép, és egy olyan objektumot ad eredményül, amely a lépést jelképezi.</span><span class="sxs-lookup"><span data-stu-id="42a71-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="42a71-110">Adja meg a lépést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="42a71-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="42a71-111">Másik lehetőségként a Step objektum vagy a ResourceId is megadható.</span><span class="sxs-lookup"><span data-stu-id="42a71-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="42a71-112">Ezt az objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerStep parancsmag használatával alkalmazhatja az objektumon végzett módosításokat.</span><span class="sxs-lookup"><span data-stu-id="42a71-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="42a71-113">Példák</span><span class="sxs-lookup"><span data-stu-id="42a71-113">EXAMPLES</span></span>

### <span data-ttu-id="42a71-114">Példa 1: lépés kérése</span><span class="sxs-lookup"><span data-stu-id="42a71-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="42a71-115">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42a71-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="42a71-116">2. példa: lépés kérése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="42a71-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="42a71-117">Ez a parancs egy ContosoService1WaitStep nevű lépést kap a ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42a71-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="42a71-118">3. példa: lépés beszerzése New-AzureRmDeploymentManagerStep által visszaadott objektum használatával</span><span class="sxs-lookup"><span data-stu-id="42a71-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="42a71-119">Ez a parancs olyan lépésekkel lép be, amelyeknek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="42a71-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="42a71-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42a71-120">PARAMETERS</span></span>

### <span data-ttu-id="42a71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a71-121">-DefaultProfile</span></span>
<span data-ttu-id="42a71-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42a71-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a71-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42a71-123">-Name</span></span>
<span data-ttu-id="42a71-124">A lépéshez tartozó név.</span><span class="sxs-lookup"><span data-stu-id="42a71-124">The name of the step.</span></span>

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

### <span data-ttu-id="42a71-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a71-125">-ResourceGroupName</span></span>
<span data-ttu-id="42a71-126">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="42a71-126">The resource group.</span></span>

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

### <span data-ttu-id="42a71-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a71-127">-ResourceId</span></span>
<span data-ttu-id="42a71-128">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="42a71-128">The resource identifier.</span></span>

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

### <span data-ttu-id="42a71-129">Lépés</span><span class="sxs-lookup"><span data-stu-id="42a71-129">-Step</span></span>
<span data-ttu-id="42a71-130">A lépés erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="42a71-130">The step resource object.</span></span>

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

### <span data-ttu-id="42a71-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a71-131">CommonParameters</span></span>
<span data-ttu-id="42a71-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42a71-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="42a71-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a71-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a71-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42a71-134">INPUTS</span></span>

### <span data-ttu-id="42a71-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42a71-135">System.String</span></span>

### <span data-ttu-id="42a71-136">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="42a71-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="42a71-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42a71-137">OUTPUTS</span></span>

### <span data-ttu-id="42a71-138">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="42a71-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="42a71-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42a71-139">NOTES</span></span>

## <span data-ttu-id="42a71-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42a71-140">RELATED LINKS</span></span>
