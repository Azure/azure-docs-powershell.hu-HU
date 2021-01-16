---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387489"
---
# <span data-ttu-id="393b2-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="393b2-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="393b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="393b2-102">SYNOPSIS</span></span>
<span data-ttu-id="393b2-103">Megkapja a bevezetést.</span><span class="sxs-lookup"><span data-stu-id="393b2-103">Gets the rollout.</span></span>

## <span data-ttu-id="393b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="393b2-104">SYNTAX</span></span>

### <span data-ttu-id="393b2-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="393b2-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393b2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="393b2-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="393b2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="393b2-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="393b2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="393b2-108">DESCRIPTION</span></span>
<span data-ttu-id="393b2-109">A **Get-AzDeploymentManagerRollout** parancsmag bevezetést kap, és egy olyan objektumot ad vissza, amely az adott bevezetést képviseli a bevezetés folyamatának részletes adataival együtt.</span><span class="sxs-lookup"><span data-stu-id="393b2-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="393b2-110">Adja meg a bevezetést a neve és az erőforráscsoport neve szerint.</span><span class="sxs-lookup"><span data-stu-id="393b2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="393b2-111">Másik módon meg is használhatja a bevezetési objektumot vagy az Erőforrásazonosítót.</span><span class="sxs-lookup"><span data-stu-id="393b2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="393b2-112">A visszaadott bevezetési objektum tartalmazza az üzembe helyezett és a folyamatban lévő szolgáltatásokat, szolgáltatási egységeket és lépéseket.</span><span class="sxs-lookup"><span data-stu-id="393b2-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="393b2-113">Az üzembe helyezésre még nem érkezett válasz.</span><span class="sxs-lookup"><span data-stu-id="393b2-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="393b2-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="393b2-114">EXAMPLES</span></span>

### <span data-ttu-id="393b2-115">1. példa: A bevezetés lekérte</span><span class="sxs-lookup"><span data-stu-id="393b2-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="393b2-116">Ez a parancs egy ContosoRollout nevű bevezetést kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="393b2-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="393b2-117">2. példa a bevezetés részleteinek be- és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="393b2-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="393b2-118">Ez a parancs egy ContosoRollout nevű bevezetést kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="393b2-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="393b2-119">A -Verbose kapcsoló hierarchikusan jeleníti meg az összes bevezetési részletet; a Szolgáltatások, a ServiceUnits és az egyes ServiceUnits alatti lépések és környezetfüggő információk az egyes lépésekhez a bevezetés holisztikus megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="393b2-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="393b2-120">3. példa: Bevezetés az erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="393b2-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="393b2-121">Ez a parancs egy ContosoRollout nevű bevezetést kap a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="393b2-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="393b2-122">4. példa: Bevezetés a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="393b2-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="393b2-123">Ez a parancs egy olyan bevezetést kap, amelynek neve és ResourceGroup tulajdonsága megegyezik a név és az ErőforráscsoportNév $rolloutObject tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="393b2-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="393b2-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="393b2-124">PARAMETERS</span></span>

### <span data-ttu-id="393b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393b2-125">-DefaultProfile</span></span>
<span data-ttu-id="393b2-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="393b2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393b2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="393b2-127">-InputObject</span></span>
<span data-ttu-id="393b2-128">Rollout objektum.</span><span class="sxs-lookup"><span data-stu-id="393b2-128">Rollout object.</span></span>

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

### <span data-ttu-id="393b2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="393b2-129">-Name</span></span>
<span data-ttu-id="393b2-130">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="393b2-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="393b2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393b2-131">-ResourceGroupName</span></span>
<span data-ttu-id="393b2-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="393b2-132">The resource group.</span></span>

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

### <span data-ttu-id="393b2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="393b2-133">-ResourceId</span></span>
<span data-ttu-id="393b2-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="393b2-134">The resource identifier.</span></span>

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

### <span data-ttu-id="393b2-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="393b2-135">-RetryAttempt</span></span>
<span data-ttu-id="393b2-136">A bevezetés újrapróbálkozási kísérlete.</span><span class="sxs-lookup"><span data-stu-id="393b2-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393b2-137">CommonParameters</span></span>
<span data-ttu-id="393b2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393b2-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="393b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393b2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="393b2-140">INPUTS</span></span>

### <span data-ttu-id="393b2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="393b2-141">System.String</span></span>

### <span data-ttu-id="393b2-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="393b2-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="393b2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="393b2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="393b2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="393b2-144">OUTPUTS</span></span>

### <span data-ttu-id="393b2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="393b2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="393b2-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="393b2-146">NOTES</span></span>

## <span data-ttu-id="393b2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="393b2-147">RELATED LINKS</span></span>
