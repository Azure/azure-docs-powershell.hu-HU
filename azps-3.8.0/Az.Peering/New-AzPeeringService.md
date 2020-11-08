---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014473"
---
# <span data-ttu-id="9b075-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="9b075-101">New-AzPeeringService</span></span>

## <span data-ttu-id="9b075-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b075-102">SYNOPSIS</span></span>
<span data-ttu-id="9b075-103">Új társközi szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9b075-103">Creates a new peering service.</span></span>

## <span data-ttu-id="9b075-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b075-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b075-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b075-105">DESCRIPTION</span></span>
<span data-ttu-id="9b075-106">A társas szolgáltatás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9b075-106">Creates peering service.</span></span>

## <span data-ttu-id="9b075-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9b075-107">EXAMPLES</span></span>

### <span data-ttu-id="9b075-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b075-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="9b075-109">Egy társközi szolgáltatási objektumot hoz létre a szolgáltatóval és a kinézeti helyekkel.</span><span class="sxs-lookup"><span data-stu-id="9b075-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="9b075-110">Használat a conjuction-ban `Get-AzPeeringServiceProvider` és a `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="9b075-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="9b075-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b075-111">PARAMETERS</span></span>

### <span data-ttu-id="9b075-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b075-112">-AsJob</span></span>
<span data-ttu-id="9b075-113">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="9b075-113">Run in the background.</span></span>

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

### <span data-ttu-id="9b075-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b075-114">-DefaultProfile</span></span>
<span data-ttu-id="9b075-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b075-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b075-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b075-116">-Name</span></span>
<span data-ttu-id="9b075-117">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="9b075-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9b075-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="9b075-118">-PeeringLocation</span></span>
<span data-ttu-id="9b075-119">Az Azure-területtől eltérő fizikai hely.</span><span class="sxs-lookup"><span data-stu-id="9b075-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="9b075-120">Get-AzPeeringServiceLocation [-Country <country> ] használata</span><span class="sxs-lookup"><span data-stu-id="9b075-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="9b075-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="9b075-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="9b075-122">A társas szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="9b075-122">The peering service provider name.</span></span>
<span data-ttu-id="9b075-123">Get-AzPeeringServiceProvider parancsmag használata listához</span><span class="sxs-lookup"><span data-stu-id="9b075-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b075-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b075-124">-ResourceGroupName</span></span>
<span data-ttu-id="9b075-125">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="9b075-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="9b075-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="9b075-126">-Tag</span></span>
<span data-ttu-id="9b075-127">A Microsoft InputObject szolgáltatással társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="9b075-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="9b075-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b075-128">-Confirm</span></span>
<span data-ttu-id="9b075-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b075-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b075-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b075-130">-WhatIf</span></span>
<span data-ttu-id="9b075-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b075-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b075-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b075-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b075-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b075-133">CommonParameters</span></span>
<span data-ttu-id="9b075-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b075-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b075-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b075-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b075-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b075-136">INPUTS</span></span>

### <span data-ttu-id="9b075-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b075-137">None</span></span>

## <span data-ttu-id="9b075-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b075-138">OUTPUTS</span></span>

### <span data-ttu-id="9b075-139">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="9b075-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="9b075-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b075-140">NOTES</span></span>

## <span data-ttu-id="9b075-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b075-141">RELATED LINKS</span></span>
