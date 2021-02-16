---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146698"
---
# <span data-ttu-id="5a462-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5a462-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="5a462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a462-102">SYNOPSIS</span></span>
<span data-ttu-id="5a462-103">Eltávolítja a virtuális hálózat társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="5a462-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="5a462-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a462-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a462-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a462-105">DESCRIPTION</span></span>
<span data-ttu-id="5a462-106">Eltávolítja a virtuális hálózat társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="5a462-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="5a462-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a462-107">EXAMPLES</span></span>

### <span data-ttu-id="5a462-108">1. példa: Virtuális hálózat társviszonyának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5a462-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="5a462-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a462-109">PARAMETERS</span></span>

### <span data-ttu-id="5a462-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a462-110">-AsJob</span></span>
<span data-ttu-id="5a462-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5a462-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a462-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a462-112">-DefaultProfile</span></span>
<span data-ttu-id="5a462-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a462-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a462-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5a462-114">-Force</span></span>
<span data-ttu-id="5a462-115">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5a462-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a462-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a462-116">-Name</span></span>
<span data-ttu-id="5a462-117">A virtuális hálózat társviszony-neve.</span><span class="sxs-lookup"><span data-stu-id="5a462-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="5a462-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a462-118">-PassThru</span></span>
<span data-ttu-id="5a462-119">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5a462-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a462-120">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5a462-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a462-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a462-121">-ResourceGroupName</span></span>
<span data-ttu-id="5a462-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5a462-122">The resource group name</span></span>

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

### <span data-ttu-id="5a462-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5a462-123">-VirtualNetworkName</span></span>
<span data-ttu-id="5a462-124">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5a462-124">The virtual network name.</span></span>

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

### <span data-ttu-id="5a462-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a462-125">-Confirm</span></span>
<span data-ttu-id="5a462-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a462-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a462-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a462-127">-WhatIf</span></span>
<span data-ttu-id="5a462-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a462-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a462-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a462-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a462-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a462-130">CommonParameters</span></span>
<span data-ttu-id="5a462-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a462-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a462-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a462-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a462-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a462-133">INPUTS</span></span>

### <span data-ttu-id="5a462-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5a462-134">System.String</span></span>

## <span data-ttu-id="5a462-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a462-135">OUTPUTS</span></span>

### <span data-ttu-id="5a462-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a462-136">System.Boolean</span></span>

## <span data-ttu-id="5a462-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a462-137">NOTES</span></span>

## <span data-ttu-id="5a462-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a462-138">RELATED LINKS</span></span>

[<span data-ttu-id="5a462-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5a462-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="5a462-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5a462-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="5a462-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5a462-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
