---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940033"
---
# <span data-ttu-id="957ed-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="957ed-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="957ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957ed-102">SYNOPSIS</span></span>
<span data-ttu-id="957ed-103">Eltávolítja a virtuális hálózat társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="957ed-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="957ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="957ed-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="957ed-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="957ed-105">DESCRIPTION</span></span>
<span data-ttu-id="957ed-106">Eltávolítja a virtuális hálózat társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="957ed-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="957ed-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="957ed-107">EXAMPLES</span></span>

### <span data-ttu-id="957ed-108">1. példa: Virtuális hálózat társviszonyának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="957ed-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="957ed-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="957ed-109">PARAMETERS</span></span>

### <span data-ttu-id="957ed-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="957ed-110">-AsJob</span></span>
<span data-ttu-id="957ed-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="957ed-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="957ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957ed-112">-DefaultProfile</span></span>
<span data-ttu-id="957ed-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="957ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="957ed-114">-Force</span><span class="sxs-lookup"><span data-stu-id="957ed-114">-Force</span></span>
<span data-ttu-id="957ed-115">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="957ed-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="957ed-116">-Name</span><span class="sxs-lookup"><span data-stu-id="957ed-116">-Name</span></span>
<span data-ttu-id="957ed-117">A virtuális hálózat társviszony-neve.</span><span class="sxs-lookup"><span data-stu-id="957ed-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ed-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="957ed-118">-PassThru</span></span>
<span data-ttu-id="957ed-119">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="957ed-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="957ed-120">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="957ed-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="957ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="957ed-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="957ed-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ed-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="957ed-123">-VirtualNetworkName</span></span>
<span data-ttu-id="957ed-124">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="957ed-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ed-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="957ed-125">-Confirm</span></span>
<span data-ttu-id="957ed-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="957ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="957ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957ed-127">-WhatIf</span></span>
<span data-ttu-id="957ed-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="957ed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="957ed-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="957ed-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="957ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957ed-130">CommonParameters</span></span>
<span data-ttu-id="957ed-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957ed-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="957ed-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957ed-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="957ed-133">INPUTS</span></span>

### <span data-ttu-id="957ed-134">System.String</span><span class="sxs-lookup"><span data-stu-id="957ed-134">System.String</span></span>

## <span data-ttu-id="957ed-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="957ed-135">OUTPUTS</span></span>

### <span data-ttu-id="957ed-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="957ed-136">System.Boolean</span></span>

## <span data-ttu-id="957ed-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="957ed-137">NOTES</span></span>

## <span data-ttu-id="957ed-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="957ed-138">RELATED LINKS</span></span>

[<span data-ttu-id="957ed-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="957ed-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="957ed-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="957ed-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="957ed-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="957ed-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
