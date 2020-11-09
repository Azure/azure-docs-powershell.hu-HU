---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297239"
---
# <span data-ttu-id="b4c18-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="b4c18-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="b4c18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4c18-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c18-103">Megkapja a kiépítést.</span><span class="sxs-lookup"><span data-stu-id="b4c18-103">Gets the rollout.</span></span>

## <span data-ttu-id="b4c18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4c18-104">SYNTAX</span></span>

### <span data-ttu-id="b4c18-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4c18-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c18-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c18-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4c18-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4c18-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4c18-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4c18-108">DESCRIPTION</span></span>
<span data-ttu-id="b4c18-109">A **Get-AzDeploymentManagerRollout** parancsmag bevezetést kap, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b4c18-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="b4c18-110">Adja meg a kiépítést a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="b4c18-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="b4c18-111">Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b4c18-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="b4c18-112">A visszaadott bevezetési objektum tartalmazza a telepített szolgáltatásokat, szolgáltatási egységeket és lépéseket, valamint a folyamatban lévőket.</span><span class="sxs-lookup"><span data-stu-id="b4c18-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="b4c18-113">Azok, amelyeket még el kell vetni, nem szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="b4c18-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="b4c18-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b4c18-114">EXAMPLES</span></span>

### <span data-ttu-id="b4c18-115">Példa 1 a kivezetéshez</span><span class="sxs-lookup"><span data-stu-id="b4c18-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="b4c18-116">Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.</span><span class="sxs-lookup"><span data-stu-id="b4c18-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="b4c18-117">2. példa a kivezetési adatok beolvasása és megjelenítése</span><span class="sxs-lookup"><span data-stu-id="b4c18-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="b4c18-118">Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.</span><span class="sxs-lookup"><span data-stu-id="b4c18-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="b4c18-119">A-verbose kapcsoló az összes kivezetési részletet hierarchikusan jeleníti meg; a szolgáltatások, a ServiceUnits és az egyes ServiceUnit, valamint a környezetfüggő információk megjelenítése az egyes lépésekhez a bevezetés holisztikus nézete érdekében.</span><span class="sxs-lookup"><span data-stu-id="b4c18-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="b4c18-120">3. példa: Bevezetés beszerzése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="b4c18-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="b4c18-121">Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.</span><span class="sxs-lookup"><span data-stu-id="b4c18-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4c18-122">Példa 4: Bevezetés a bevezetési objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="b4c18-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="b4c18-123">Ez a parancs olyan kivezetést kap, akinek a neve és a ResourceGroup megegyezik a $rolloutObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="b4c18-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="b4c18-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4c18-124">PARAMETERS</span></span>

### <span data-ttu-id="b4c18-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c18-125">-DefaultProfile</span></span>
<span data-ttu-id="b4c18-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4c18-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c18-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4c18-127">-InputObject</span></span>
<span data-ttu-id="b4c18-128">Objektum kiépítése</span><span class="sxs-lookup"><span data-stu-id="b4c18-128">Rollout object.</span></span>

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

### <span data-ttu-id="b4c18-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4c18-129">-Name</span></span>
<span data-ttu-id="b4c18-130">A bevezetés neve.</span><span class="sxs-lookup"><span data-stu-id="b4c18-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="b4c18-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c18-131">-ResourceGroupName</span></span>
<span data-ttu-id="b4c18-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="b4c18-132">The resource group.</span></span>

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

### <span data-ttu-id="b4c18-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c18-133">-ResourceId</span></span>
<span data-ttu-id="b4c18-134">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b4c18-134">The resource identifier.</span></span>

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

### <span data-ttu-id="b4c18-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="b4c18-135">-RetryAttempt</span></span>
<span data-ttu-id="b4c18-136">A bevezetés kísérlete a bevezetéshez.</span><span class="sxs-lookup"><span data-stu-id="b4c18-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="b4c18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c18-137">CommonParameters</span></span>
<span data-ttu-id="b4c18-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4c18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c18-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4c18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c18-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4c18-140">INPUTS</span></span>

### <span data-ttu-id="b4c18-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4c18-141">System.String</span></span>

### <span data-ttu-id="b4c18-142">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b4c18-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b4c18-143">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="b4c18-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b4c18-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4c18-144">OUTPUTS</span></span>

### <span data-ttu-id="b4c18-145">Microsoft. Azure. Command. DeploymentManager. models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="b4c18-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b4c18-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4c18-146">NOTES</span></span>

## <span data-ttu-id="b4c18-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4c18-147">RELATED LINKS</span></span>
