---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 24fcfc222d9d3cab1b0785c121e09b596aae16fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937634"
---
# <span data-ttu-id="a5d05-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a5d05-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="a5d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d05-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d05-103">Új társviszony-létesítő szolgáltatás előtagja</span><span class="sxs-lookup"><span data-stu-id="a5d05-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="a5d05-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5d05-104">SYNTAX</span></span>

### <span data-ttu-id="a5d05-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5d05-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d05-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d05-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d05-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d05-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d05-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5d05-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d05-109">Társviszony-létesítő szolgáltatás-előtagot hoz létre egy társviszony-létesítő szolgáltatásobjektumhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="a5d05-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="a5d05-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5d05-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d05-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5d05-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a5d05-112">Előtag létrehozása társviszony-szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="a5d05-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="a5d05-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a5d05-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a5d05-114">Előtagot hoz létre egy társviszony-szolgáltatás erőforrás-azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="a5d05-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="a5d05-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a5d05-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a5d05-116">Előtagot hoz létre egy társviszony-szolgáltatáserőforrás-csoport nevéből és nevéből</span><span class="sxs-lookup"><span data-stu-id="a5d05-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="a5d05-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d05-117">PARAMETERS</span></span>

### <span data-ttu-id="a5d05-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d05-118">-AsJob</span></span>
<span data-ttu-id="a5d05-119">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a5d05-119">Run in the background.</span></span>

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

### <span data-ttu-id="a5d05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d05-120">-DefaultProfile</span></span>
<span data-ttu-id="a5d05-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5d05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d05-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a5d05-122">-Name</span></span>
<span data-ttu-id="a5d05-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a5d05-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a5d05-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="a5d05-124">-PeeringServiceId</span></span>
<span data-ttu-id="a5d05-125">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="a5d05-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d05-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="a5d05-126">-PeeringServiceName</span></span>
<span data-ttu-id="a5d05-127">A társviszony-létesítő szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a5d05-127">The peering service name.</span></span>
<span data-ttu-id="a5d05-128">Egy New-AzPeeringService új társviszony-szolgáltatáshoz Get-AzPeeringService parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a5d05-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d05-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="a5d05-129">-PeeringServiceObject</span></span>
<span data-ttu-id="a5d05-130">A Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="a5d05-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d05-131">-Előtag</span><span class="sxs-lookup"><span data-stu-id="a5d05-131">-Prefix</span></span>
<span data-ttu-id="a5d05-132">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="a5d05-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="a5d05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d05-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5d05-134">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="a5d05-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d05-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="a5d05-135">-ServiceKey</span></span>
<span data-ttu-id="a5d05-136">Ez egy egyedi GUID azonosító, amelyet a szolgáltató biztosít</span><span class="sxs-lookup"><span data-stu-id="a5d05-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="a5d05-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5d05-137">-Confirm</span></span>
<span data-ttu-id="a5d05-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5d05-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d05-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d05-139">-WhatIf</span></span>
<span data-ttu-id="a5d05-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5d05-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d05-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5d05-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d05-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d05-142">CommonParameters</span></span>
<span data-ttu-id="a5d05-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d05-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d05-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d05-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d05-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d05-145">INPUTS</span></span>

### <span data-ttu-id="a5d05-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="a5d05-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="a5d05-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5d05-147">OUTPUTS</span></span>

### <span data-ttu-id="a5d05-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a5d05-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="a5d05-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5d05-149">NOTES</span></span>

## <span data-ttu-id="a5d05-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5d05-150">RELATED LINKS</span></span>
