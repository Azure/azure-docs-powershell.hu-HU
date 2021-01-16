---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354270"
---
# <span data-ttu-id="e5532-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="e5532-101">New-AzPeeringService</span></span>

## <span data-ttu-id="e5532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5532-102">SYNOPSIS</span></span>
<span data-ttu-id="e5532-103">Létrehoz egy új társviszony-létesítő szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e5532-103">Creates a new peering service.</span></span>

## <span data-ttu-id="e5532-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5532-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5532-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5532-105">DESCRIPTION</span></span>
<span data-ttu-id="e5532-106">Társviszony-létesítő szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5532-106">Creates peering service.</span></span>

## <span data-ttu-id="e5532-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5532-107">EXAMPLES</span></span>

### <span data-ttu-id="e5532-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5532-108">Example 1</span></span>
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

<span data-ttu-id="e5532-109">Társviszony-létesítő szolgáltatásobjektumot hoz létre szolgáltatóval és társviszony-létesítés helyével.</span><span class="sxs-lookup"><span data-stu-id="e5532-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="e5532-110">Használat konjugáltban a `Get-AzPeeringServiceProvider``Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="e5532-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="e5532-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5532-111">PARAMETERS</span></span>

### <span data-ttu-id="e5532-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5532-112">-AsJob</span></span>
<span data-ttu-id="e5532-113">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e5532-113">Run in the background.</span></span>

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

### <span data-ttu-id="e5532-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5532-114">-DefaultProfile</span></span>
<span data-ttu-id="e5532-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5532-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5532-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e5532-116">-Name</span></span>
<span data-ttu-id="e5532-117">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="e5532-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e5532-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e5532-118">-PeeringLocation</span></span>
<span data-ttu-id="e5532-119">Az Azure Régiótól eltérő fizikai hely.</span><span class="sxs-lookup"><span data-stu-id="e5532-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="e5532-120">Használja Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="e5532-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="e5532-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="e5532-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="e5532-122">A társviszony-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="e5532-122">The peering service provider name.</span></span>
<span data-ttu-id="e5532-123">Lista Get-AzPeeringServiceProvider parancsmag használata</span><span class="sxs-lookup"><span data-stu-id="e5532-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

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

### <span data-ttu-id="e5532-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5532-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5532-125">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="e5532-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e5532-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5532-126">-Tag</span></span>
<span data-ttu-id="e5532-127">A Microsoft InputObject szolgáltatáshoz társítható címkék.</span><span class="sxs-lookup"><span data-stu-id="e5532-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="e5532-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5532-128">-Confirm</span></span>
<span data-ttu-id="e5532-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e5532-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5532-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5532-130">-WhatIf</span></span>
<span data-ttu-id="e5532-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e5532-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5532-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5532-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5532-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5532-133">CommonParameters</span></span>
<span data-ttu-id="e5532-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5532-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5532-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5532-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5532-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5532-136">INPUTS</span></span>

### <span data-ttu-id="e5532-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5532-137">None</span></span>

## <span data-ttu-id="e5532-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5532-138">OUTPUTS</span></span>

### <span data-ttu-id="e5532-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="e5532-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="e5532-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5532-140">NOTES</span></span>

## <span data-ttu-id="e5532-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5532-141">RELATED LINKS</span></span>
