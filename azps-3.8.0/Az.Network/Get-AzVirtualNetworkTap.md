---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011367"
---
# <span data-ttu-id="2e38d-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e38d-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="2e38d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e38d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e38d-103">Virtuális hálózat beolvasása koppintással</span><span class="sxs-lookup"><span data-stu-id="2e38d-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="2e38d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e38d-104">SYNTAX</span></span>

### <span data-ttu-id="2e38d-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e38d-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e38d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e38d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e38d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e38d-107">DESCRIPTION</span></span>
<span data-ttu-id="2e38d-108">A **Get-AzVirtualNetworkTap** parancsmag Azure virtuális hálózati koppintással vagy Azure virtuális hálózati koppintásokat tartalmazó listával jelenik meg egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="2e38d-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="2e38d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2e38d-109">EXAMPLES</span></span>

### <span data-ttu-id="2e38d-110">Példa 1: virtuális hálózat beszerzése koppintással</span><span class="sxs-lookup"><span data-stu-id="2e38d-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="2e38d-111">Ez a parancs a "ResourceGroup1"-ban a "VirtualTap1" kifejezésre koppintva egy VirtualNetwork-koppintást kap.</span><span class="sxs-lookup"><span data-stu-id="2e38d-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="2e38d-112">2. példa: a virtuális hálózati csapok szűréssel való lekérése</span><span class="sxs-lookup"><span data-stu-id="2e38d-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="2e38d-113">Ez a parancs minden VirtualNetwork koppint a "VirtualTap" kezdetű hivatkozásokra.</span><span class="sxs-lookup"><span data-stu-id="2e38d-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="2e38d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e38d-114">PARAMETERS</span></span>

### <span data-ttu-id="2e38d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e38d-115">-DefaultProfile</span></span>
<span data-ttu-id="2e38d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e38d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e38d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e38d-117">-Name</span></span>
<span data-ttu-id="2e38d-118">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="2e38d-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2e38d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e38d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e38d-120">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="2e38d-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2e38d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e38d-121">-ResourceId</span></span>
<span data-ttu-id="2e38d-122">A VirtualNetworkTap-erőforrás ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e38d-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e38d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e38d-123">-Confirm</span></span>
<span data-ttu-id="2e38d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e38d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e38d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e38d-125">-WhatIf</span></span>
<span data-ttu-id="2e38d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e38d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e38d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e38d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e38d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e38d-128">CommonParameters</span></span>
<span data-ttu-id="2e38d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e38d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e38d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e38d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e38d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e38d-131">INPUTS</span></span>

### <span data-ttu-id="2e38d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2e38d-132">System.String</span></span>

## <span data-ttu-id="2e38d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e38d-133">OUTPUTS</span></span>

### <span data-ttu-id="2e38d-134">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e38d-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2e38d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e38d-135">NOTES</span></span>

## <span data-ttu-id="2e38d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e38d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e38d-137">Új – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e38d-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="2e38d-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e38d-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="2e38d-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e38d-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
