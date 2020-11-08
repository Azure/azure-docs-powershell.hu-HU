---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185016"
---
# <span data-ttu-id="69be5-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="69be5-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="69be5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69be5-102">SYNOPSIS</span></span>
<span data-ttu-id="69be5-103">Létrehoz egy szolgáltatást a megadott szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="69be5-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="69be5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69be5-104">SYNTAX</span></span>

### <span data-ttu-id="69be5-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69be5-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69be5-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="69be5-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69be5-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="69be5-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69be5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69be5-108">DESCRIPTION</span></span>
<span data-ttu-id="69be5-109">A **New-AzDeploymentManagerService** parancsmag egy szolgáltatás topológiája alatt hoz létre egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.</span><span class="sxs-lookup"><span data-stu-id="69be5-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="69be5-110">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="69be5-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="69be5-111">A parancsmag egy szolgáltatási objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="69be5-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="69be5-112">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="69be5-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="69be5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="69be5-113">EXAMPLES</span></span>

### <span data-ttu-id="69be5-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69be5-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="69be5-115">Új szolgáltatást hoz létre, amelynek neve ContosoService1 a szolgáltatás topológiája ContosoServiceTopology az erőforráscsoport ContosoResourceGroup, a közép-amerikai helyen.</span><span class="sxs-lookup"><span data-stu-id="69be5-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="69be5-116">A TargetLocation tulajdonság azt jelzi, hogy a szolgáltatás ContosoService1 az adott előfizetésben a kelet-amerikai régióba kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="69be5-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="69be5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69be5-117">PARAMETERS</span></span>

### <span data-ttu-id="69be5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69be5-118">-DefaultProfile</span></span>
<span data-ttu-id="69be5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69be5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69be5-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="69be5-120">-Location</span></span>
<span data-ttu-id="69be5-121">A szolgáltatási erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="69be5-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69be5-122">-Name</span></span>
<span data-ttu-id="69be5-123">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="69be5-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69be5-124">-ResourceGroupName</span></span>
<span data-ttu-id="69be5-125">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="69be5-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="69be5-126">-ServiceTopologyId</span></span>
<span data-ttu-id="69be5-127">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="69be5-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="69be5-128">-ServiceTopologyName</span></span>
<span data-ttu-id="69be5-129">Annak a szolgáltatásnak a neve, amelyhez a szolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="69be5-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="69be5-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="69be5-131">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="69be5-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="69be5-132">-Tag</span></span>
<span data-ttu-id="69be5-133">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="69be5-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="69be5-134">-TargetLocation</span></span>
<span data-ttu-id="69be5-135">Annak a helynek a meghatározása, ahol a szolgáltatás alatti erőforrásokat telepítették.</span><span class="sxs-lookup"><span data-stu-id="69be5-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69be5-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="69be5-137">Azt az előfizetést határozza meg, amelyre a szolgáltatás alatti erőforrásokat telepítették.</span><span class="sxs-lookup"><span data-stu-id="69be5-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69be5-138">-Confirm</span></span>
<span data-ttu-id="69be5-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69be5-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69be5-140">-WhatIf</span></span>
<span data-ttu-id="69be5-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69be5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69be5-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69be5-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be5-143">CommonParameters</span></span>
<span data-ttu-id="69be5-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69be5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be5-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69be5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be5-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69be5-146">INPUTS</span></span>

### <span data-ttu-id="69be5-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="69be5-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69be5-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69be5-148">OUTPUTS</span></span>

### <span data-ttu-id="69be5-149">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="69be5-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="69be5-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69be5-150">NOTES</span></span>

## <span data-ttu-id="69be5-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69be5-151">RELATED LINKS</span></span>
