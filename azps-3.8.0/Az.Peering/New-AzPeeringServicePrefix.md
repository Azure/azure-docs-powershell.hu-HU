---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: e488baacb4e9412cb4e3e5be2b6a595629495b16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012762"
---
# <span data-ttu-id="7735f-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7735f-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="7735f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7735f-102">SYNOPSIS</span></span>
<span data-ttu-id="7735f-103">Új társközi szolgáltatás-előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7735f-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="7735f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7735f-104">SYNTAX</span></span>

### <span data-ttu-id="7735f-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7735f-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7735f-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7735f-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7735f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7735f-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7735f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7735f-108">DESCRIPTION</span></span>
<span data-ttu-id="7735f-109">Egy egyenrangú szolgáltatási objektumhoz társított, a szolgáltatáshoz tartozó előtagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7735f-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="7735f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7735f-110">EXAMPLES</span></span>

### <span data-ttu-id="7735f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7735f-111">Example 1</span></span>
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

<span data-ttu-id="7735f-112">Előtag létrehozása egy társközi szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="7735f-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="7735f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7735f-113">Example 2</span></span>
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

<span data-ttu-id="7735f-114">Egy társközi szolgáltatási erőforrás-azonosítóból hoz létre előtagot.</span><span class="sxs-lookup"><span data-stu-id="7735f-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="7735f-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7735f-115">Example 3</span></span>
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

<span data-ttu-id="7735f-116">Előtagot hoz létre egy társközi szolgáltatás-erőforráscsoport nevéből és nevéből</span><span class="sxs-lookup"><span data-stu-id="7735f-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="7735f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7735f-117">PARAMETERS</span></span>

### <span data-ttu-id="7735f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7735f-118">-AsJob</span></span>
<span data-ttu-id="7735f-119">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="7735f-119">Run in the background.</span></span>

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

### <span data-ttu-id="7735f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7735f-120">-DefaultProfile</span></span>
<span data-ttu-id="7735f-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7735f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7735f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7735f-122">-Name</span></span>
<span data-ttu-id="7735f-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="7735f-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7735f-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="7735f-124">-PeeringServiceId</span></span>
<span data-ttu-id="7735f-125">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="7735f-125">The resource id string name.</span></span>

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

### <span data-ttu-id="7735f-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="7735f-126">-PeeringServiceName</span></span>
<span data-ttu-id="7735f-127">A társas szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7735f-127">The peering service name.</span></span>
<span data-ttu-id="7735f-128">New-AzPeeringService parancsmagot használhat új társközi szolgáltatáshoz vagy Get-AzPeeringService a listákhoz.</span><span class="sxs-lookup"><span data-stu-id="7735f-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="7735f-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="7735f-129">-PeeringServiceObject</span></span>
<span data-ttu-id="7735f-130">Get-AzPeeringService használata</span><span class="sxs-lookup"><span data-stu-id="7735f-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="7735f-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7735f-131">-Prefix</span></span>
<span data-ttu-id="7735f-132">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="7735f-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="7735f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7735f-133">-ResourceGroupName</span></span>
<span data-ttu-id="7735f-134">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="7735f-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7735f-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7735f-135">-Confirm</span></span>
<span data-ttu-id="7735f-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7735f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7735f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7735f-137">-WhatIf</span></span>
<span data-ttu-id="7735f-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7735f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7735f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7735f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7735f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7735f-140">CommonParameters</span></span>
<span data-ttu-id="7735f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7735f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7735f-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7735f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7735f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7735f-143">INPUTS</span></span>

### <span data-ttu-id="7735f-144">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="7735f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="7735f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7735f-145">OUTPUTS</span></span>

### <span data-ttu-id="7735f-146">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7735f-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="7735f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7735f-147">NOTES</span></span>

## <span data-ttu-id="7735f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7735f-148">RELATED LINKS</span></span>
