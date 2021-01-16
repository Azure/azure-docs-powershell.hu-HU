---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361113"
---
# <span data-ttu-id="6301f-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6301f-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="6301f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6301f-102">SYNOPSIS</span></span>
<span data-ttu-id="6301f-103">Virtuális hálózatra koppint</span><span class="sxs-lookup"><span data-stu-id="6301f-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="6301f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6301f-104">SYNTAX</span></span>

### <span data-ttu-id="6301f-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6301f-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6301f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6301f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6301f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6301f-107">DESCRIPTION</span></span>
<span data-ttu-id="6301f-108">A **Get-AzVirtualNetworkTap** parancsmag egy Azure virtuális hálózatra való rákoppintást vagy az Azure virtuális hálózatának listáját egy erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6301f-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="6301f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6301f-109">EXAMPLES</span></span>

### <span data-ttu-id="6301f-110">1. példa: Virtuális hálózat koppintás</span><span class="sxs-lookup"><span data-stu-id="6301f-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="6301f-111">Ez a parancs virtualnetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="6301f-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="6301f-112">2. példa: Az összes virtuális hálózatra koppintás szűréssel</span><span class="sxs-lookup"><span data-stu-id="6301f-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="6301f-113">Ez a parancs a VirtualNetwork összes olyan koppintással való hivatkozását beveszi, amely a "VirtualTap" kezdettől kezdődik.</span><span class="sxs-lookup"><span data-stu-id="6301f-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="6301f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6301f-114">PARAMETERS</span></span>

### <span data-ttu-id="6301f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6301f-115">-DefaultProfile</span></span>
<span data-ttu-id="6301f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6301f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6301f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6301f-117">-Name</span></span>
<span data-ttu-id="6301f-118">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="6301f-118">The name of the tap.</span></span>

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

### <span data-ttu-id="6301f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6301f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6301f-120">A virtuális hálózat erőforráscsoportneve koppintás.</span><span class="sxs-lookup"><span data-stu-id="6301f-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="6301f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6301f-121">-ResourceId</span></span>
<span data-ttu-id="6301f-122">A VirtualNetworkTap erőforrás Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="6301f-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="6301f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6301f-123">-Confirm</span></span>
<span data-ttu-id="6301f-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6301f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6301f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6301f-125">-WhatIf</span></span>
<span data-ttu-id="6301f-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6301f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6301f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6301f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6301f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6301f-128">CommonParameters</span></span>
<span data-ttu-id="6301f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6301f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6301f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6301f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6301f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6301f-131">INPUTS</span></span>

### <span data-ttu-id="6301f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6301f-132">System.String</span></span>

## <span data-ttu-id="6301f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6301f-133">OUTPUTS</span></span>

### <span data-ttu-id="6301f-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6301f-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="6301f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6301f-135">NOTES</span></span>

## <span data-ttu-id="6301f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6301f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6301f-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6301f-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="6301f-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6301f-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="6301f-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6301f-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
