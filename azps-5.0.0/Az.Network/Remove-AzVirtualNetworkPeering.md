---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194009"
---
# <span data-ttu-id="e15a2-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e15a2-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e15a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e15a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e15a2-103">Eltávolítja a virtuális hálózat társközi nézetét.</span><span class="sxs-lookup"><span data-stu-id="e15a2-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e15a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e15a2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e15a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e15a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e15a2-106">Eltávolítja a virtuális hálózat társközi nézetét.</span><span class="sxs-lookup"><span data-stu-id="e15a2-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e15a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e15a2-107">EXAMPLES</span></span>

### <span data-ttu-id="e15a2-108">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e15a2-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e15a2-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e15a2-109">PARAMETERS</span></span>

### <span data-ttu-id="e15a2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e15a2-110">-AsJob</span></span>
<span data-ttu-id="e15a2-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e15a2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e15a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e15a2-112">-DefaultProfile</span></span>
<span data-ttu-id="e15a2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e15a2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e15a2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e15a2-114">-Force</span></span>
<span data-ttu-id="e15a2-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e15a2-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e15a2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e15a2-116">-Name</span></span>
<span data-ttu-id="e15a2-117">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="e15a2-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="e15a2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e15a2-118">-PassThru</span></span>
<span data-ttu-id="e15a2-119">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e15a2-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e15a2-120">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e15a2-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e15a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e15a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e15a2-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e15a2-122">The resource group name</span></span>

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

### <span data-ttu-id="e15a2-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e15a2-123">-VirtualNetworkName</span></span>
<span data-ttu-id="e15a2-124">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="e15a2-124">The virtual network name.</span></span>

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

### <span data-ttu-id="e15a2-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e15a2-125">-Confirm</span></span>
<span data-ttu-id="e15a2-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e15a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e15a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e15a2-127">-WhatIf</span></span>
<span data-ttu-id="e15a2-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e15a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e15a2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e15a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e15a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15a2-130">CommonParameters</span></span>
<span data-ttu-id="e15a2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e15a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15a2-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e15a2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15a2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e15a2-133">INPUTS</span></span>

### <span data-ttu-id="e15a2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e15a2-134">System.String</span></span>

## <span data-ttu-id="e15a2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e15a2-135">OUTPUTS</span></span>

### <span data-ttu-id="e15a2-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e15a2-136">System.Boolean</span></span>

## <span data-ttu-id="e15a2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e15a2-137">NOTES</span></span>

## <span data-ttu-id="e15a2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e15a2-138">RELATED LINKS</span></span>

[<span data-ttu-id="e15a2-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e15a2-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e15a2-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e15a2-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e15a2-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e15a2-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
