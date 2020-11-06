---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490696"
---
# <span data-ttu-id="ab057-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ab057-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="ab057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab057-102">SYNOPSIS</span></span>
<span data-ttu-id="ab057-103">Bevezetést kap.</span><span class="sxs-lookup"><span data-stu-id="ab057-103">Gets a rollout.</span></span>

## <span data-ttu-id="ab057-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab057-104">SYNTAX</span></span>

### <span data-ttu-id="ab057-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab057-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab057-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab057-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab057-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ab057-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab057-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab057-108">DESCRIPTION</span></span>
<span data-ttu-id="ab057-109">A **Get-AzureRmDeploymentManagerRollout** parancsmag bevezetést kap, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab057-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ab057-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="ab057-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ab057-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ab057-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="ab057-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ab057-112">EXAMPLES</span></span>

### <span data-ttu-id="ab057-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab057-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ab057-114">Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.</span><span class="sxs-lookup"><span data-stu-id="ab057-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ab057-115">2. példa: Bevezetés beszerzése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="ab057-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ab057-116">Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.</span><span class="sxs-lookup"><span data-stu-id="ab057-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ab057-117">3. példa: Bevezetés a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ab057-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="ab057-118">Ez a parancs olyan kivezetést kap, akinek a neve és a ResourceGroup megegyezik a $rolloutObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="ab057-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ab057-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab057-119">PARAMETERS</span></span>

### <span data-ttu-id="ab057-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab057-120">-DefaultProfile</span></span>
<span data-ttu-id="ab057-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab057-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab057-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab057-122">-Name</span></span>
<span data-ttu-id="ab057-123">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="ab057-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="ab057-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab057-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab057-125">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="ab057-125">The resource group.</span></span>

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

### <span data-ttu-id="ab057-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab057-126">-ResourceId</span></span>
<span data-ttu-id="ab057-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ab057-127">The resource identifier.</span></span>

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

### <span data-ttu-id="ab057-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="ab057-128">-RetryAttempt</span></span>
<span data-ttu-id="ab057-129">A bevezetés kísérlete a bevezetéshez.</span><span class="sxs-lookup"><span data-stu-id="ab057-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab057-130">-Bevezetés</span><span class="sxs-lookup"><span data-stu-id="ab057-130">-Rollout</span></span>
<span data-ttu-id="ab057-131">Objektum kiépítése</span><span class="sxs-lookup"><span data-stu-id="ab057-131">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab057-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab057-132">CommonParameters</span></span>
<span data-ttu-id="ab057-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab057-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab057-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab057-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab057-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab057-135">INPUTS</span></span>

### <span data-ttu-id="ab057-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab057-136">None</span></span>

## <span data-ttu-id="ab057-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab057-137">OUTPUTS</span></span>

### <span data-ttu-id="ab057-138">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ab057-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ab057-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab057-139">NOTES</span></span>

## <span data-ttu-id="ab057-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab057-140">RELATED LINKS</span></span>

[<span data-ttu-id="ab057-141">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ab057-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="ab057-142">Újraindítás – AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ab057-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="ab057-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ab057-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)