---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932977"
---
# <span data-ttu-id="a9555-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a9555-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="a9555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9555-102">SYNOPSIS</span></span>
<span data-ttu-id="a9555-103">Létrehoz egy szolgáltatást a megadott szolgáltatás topológia alapján.</span><span class="sxs-lookup"><span data-stu-id="a9555-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="a9555-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9555-104">SYNTAX</span></span>

### <span data-ttu-id="a9555-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9555-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9555-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="a9555-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9555-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a9555-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9555-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9555-108">DESCRIPTION</span></span>
<span data-ttu-id="a9555-109">A **New-AzDeploymentManagerService parancsmag** szolgáltatás-topológia alapján hoz létre egy szolgáltatást, és visszaadja az adott szolgáltatást képviselő objektumot.</span><span class="sxs-lookup"><span data-stu-id="a9555-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="a9555-110">Adja meg a szolgáltatást a neve, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="a9555-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="a9555-111">A parancsmag szolgáltatásobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a9555-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="a9555-112">Ezt az objektumot helyben módosíthatja, majd a Set-AzDeploymentManagerService alkalmazhatja a szolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="a9555-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="a9555-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9555-113">EXAMPLES</span></span>

### <span data-ttu-id="a9555-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9555-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="a9555-115">Létrehozza a ContosoService1 nevű új szolgáltatást a ContosoServiceTopology szolgáltatás topológiája alatt a ContosoResourceGroup erőforráscsoportban, az Egyesült Államok középső területén.</span><span class="sxs-lookup"><span data-stu-id="a9555-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="a9555-116">A TargetLocation tulajdonság azt jelzi, hogy a ContosoService1 szolgáltatást a megadott előfizetésben az Egyesült Államok keleti régiójában kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="a9555-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="a9555-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9555-117">PARAMETERS</span></span>

### <span data-ttu-id="a9555-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9555-118">-DefaultProfile</span></span>
<span data-ttu-id="a9555-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9555-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9555-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a9555-120">-Location</span></span>
<span data-ttu-id="a9555-121">A szolgáltatáserőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a9555-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="a9555-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a9555-122">-Name</span></span>
<span data-ttu-id="a9555-123">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a9555-123">The name of the service.</span></span>

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

### <span data-ttu-id="a9555-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9555-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9555-125">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="a9555-125">The resource group.</span></span>

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

### <span data-ttu-id="a9555-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="a9555-126">-ServiceTopologyId</span></span>
<span data-ttu-id="a9555-127">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a9555-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="a9555-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="a9555-128">-ServiceTopologyName</span></span>
<span data-ttu-id="a9555-129">Annak a szolgáltatás topológiának a neve, amelyhez a szolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="a9555-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="a9555-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="a9555-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="a9555-131">Az a szolgáltatás topológia objektum, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a9555-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="a9555-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9555-132">-Tag</span></span>
<span data-ttu-id="a9555-133">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="a9555-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a9555-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="a9555-134">-TargetLocation</span></span>
<span data-ttu-id="a9555-135">Meghatározza azt a helyet, ahol a szolgáltatásban található erőforrások telepítve lesznek.</span><span class="sxs-lookup"><span data-stu-id="a9555-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="a9555-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9555-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="a9555-137">Meghatározza, hogy a szolgáltatás mely erőforrásokra legyen telepítve.</span><span class="sxs-lookup"><span data-stu-id="a9555-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="a9555-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9555-138">-Confirm</span></span>
<span data-ttu-id="a9555-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9555-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9555-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9555-140">-WhatIf</span></span>
<span data-ttu-id="a9555-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9555-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9555-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9555-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9555-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9555-143">CommonParameters</span></span>
<span data-ttu-id="a9555-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9555-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9555-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9555-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9555-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9555-146">INPUTS</span></span>

### <span data-ttu-id="a9555-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9555-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a9555-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9555-148">OUTPUTS</span></span>

### <span data-ttu-id="a9555-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a9555-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a9555-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9555-150">NOTES</span></span>

## <span data-ttu-id="a9555-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9555-151">RELATED LINKS</span></span>
