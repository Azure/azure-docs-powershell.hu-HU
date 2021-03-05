---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011141"
---
# <span data-ttu-id="5d8e4-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="5d8e4-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="5d8e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8e4-103">Appszolgáltatás-környezetet hoz létre, beleértve az ajánlott útválasztási táblát és hálózati biztonsági csoportot</span><span class="sxs-lookup"><span data-stu-id="5d8e4-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="5d8e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d8e4-104">SYNTAX</span></span>

### <span data-ttu-id="5d8e4-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8e4-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8e4-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8e4-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8e4-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8e4-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8e4-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d8e4-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8e4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d8e4-109">DESCRIPTION</span></span>
<span data-ttu-id="5d8e4-110">A **New-AzAppServiceEnvironment** parancsmag appszolgáltatási környezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="5d8e4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d8e4-111">EXAMPLES</span></span>

### <span data-ttu-id="5d8e4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d8e4-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="5d8e4-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span><span class="sxs-lookup"><span data-stu-id="5d8e4-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="5d8e4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5d8e4-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="5d8e4-115">A MyAseV2 nevű appszolgáltatás-környezet létrehozása ajánlott útválasztási tábla és hálózati biztonsági csoport nélkül.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="5d8e4-116">Ezeket az appszolgáltatás-környezet kiépítése előtt vagy közvetlenül az után kell létrehoznia, hogy a megfelelő példány működőképes legyen.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="5d8e4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d8e4-117">PARAMETERS</span></span>

### <span data-ttu-id="5d8e4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d8e4-118">-AsJob</span></span>
<span data-ttu-id="5d8e4-119">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8e4-120">-DefaultProfile</span></span>
<span data-ttu-id="5d8e4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8e4-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="5d8e4-122">-Kind</span></span>
<span data-ttu-id="5d8e4-123">Az app szolgáltatási környezetének verziója.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="5d8e4-124">-LoadBalancerMode</span></span>
<span data-ttu-id="5d8e4-125">Az app szolgáltatási környezet terheléselosztási módja.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-126">-Location</span><span class="sxs-lookup"><span data-stu-id="5d8e4-126">-Location</span></span>
<span data-ttu-id="5d8e4-127">Az appszolgáltatás környezetének helye, például: Nyugat-Európa.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5d8e4-128">-Name</span></span>
<span data-ttu-id="5d8e4-129">Az app szolgáltatási környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d8e4-130">-PassThru</span></span>
<span data-ttu-id="5d8e4-131">Adja vissza az app szolgáltatási környezetének objektumát.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-131">Return the app service environment object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d8e4-132">-ResourceGroupName</span></span>
<span data-ttu-id="5d8e4-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d8e4-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d8e4-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="5d8e4-135">Ne hozza létre az ajánlott hálózatbiztonsági csoportot az app szolgáltatási környezete részeként.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d8e4-136">-SkipRouteTable</span></span>
<span data-ttu-id="5d8e4-137">Ne hozza létre az ajánlott útvonaltáblát az app szolgáltatási környezete részeként.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5d8e4-138">-SubnetId</span></span>
<span data-ttu-id="5d8e4-139">Az alhálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5d8e4-140">-SubnetName</span></span>
<span data-ttu-id="5d8e4-141">Az alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-141">The subnet name.</span></span> <span data-ttu-id="5d8e4-142">A -VirtualNetworkName névvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="5d8e4-143">Ha nem, használja az -SubnetId</span><span class="sxs-lookup"><span data-stu-id="5d8e4-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5d8e4-144">-VirtualNetworkName</span></span>
<span data-ttu-id="5d8e4-145">A vNet neve.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-145">The vNet name.</span></span> <span data-ttu-id="5d8e4-146">-Alhálózatnévvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="5d8e4-147">Ha nem, használja az -SubnetId</span><span class="sxs-lookup"><span data-stu-id="5d8e4-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8e4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d8e4-148">-Confirm</span></span>
<span data-ttu-id="5d8e4-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8e4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8e4-150">-WhatIf</span></span>
<span data-ttu-id="5d8e4-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d8e4-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8e4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8e4-153">CommonParameters</span></span>
<span data-ttu-id="5d8e4-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8e4-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d8e4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8e4-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d8e4-156">INPUTS</span></span>

### <span data-ttu-id="5d8e4-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d8e4-157">None</span></span>

## <span data-ttu-id="5d8e4-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d8e4-158">OUTPUTS</span></span>

### <span data-ttu-id="5d8e4-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="5d8e4-159">System.Object</span></span>
## <span data-ttu-id="5d8e4-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d8e4-160">NOTES</span></span>

## <span data-ttu-id="5d8e4-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d8e4-161">RELATED LINKS</span></span>

[<span data-ttu-id="5d8e4-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="5d8e4-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="5d8e4-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="5d8e4-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="5d8e4-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="5d8e4-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
