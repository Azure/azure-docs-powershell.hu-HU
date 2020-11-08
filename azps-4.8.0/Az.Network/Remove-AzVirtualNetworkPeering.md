---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182983"
---
# <span data-ttu-id="c1b9f-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c1b9f-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="c1b9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b9f-103">Eltávolítja a virtuális hálózat társközi nézetét.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="c1b9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1b9f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b9f-106">Eltávolítja a virtuális hálózat társközi nézetét.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="c1b9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1b9f-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b9f-108">Példa 1: virtuális hálózat társközi eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c1b9f-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="c1b9f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1b9f-109">PARAMETERS</span></span>

### <span data-ttu-id="c1b9f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b9f-110">-AsJob</span></span>
<span data-ttu-id="c1b9f-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1b9f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1b9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b9f-112">-DefaultProfile</span></span>
<span data-ttu-id="c1b9f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b9f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c1b9f-114">-Force</span></span>
<span data-ttu-id="c1b9f-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1b9f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1b9f-116">-Name</span></span>
<span data-ttu-id="c1b9f-117">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="c1b9f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1b9f-118">-PassThru</span></span>
<span data-ttu-id="c1b9f-119">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1b9f-120">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1b9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1b9f-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c1b9f-122">The resource group name</span></span>

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

### <span data-ttu-id="c1b9f-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c1b9f-123">-VirtualNetworkName</span></span>
<span data-ttu-id="c1b9f-124">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-124">The virtual network name.</span></span>

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

### <span data-ttu-id="c1b9f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1b9f-125">-Confirm</span></span>
<span data-ttu-id="c1b9f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b9f-127">-WhatIf</span></span>
<span data-ttu-id="c1b9f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b9f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1b9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b9f-130">CommonParameters</span></span>
<span data-ttu-id="c1b9f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1b9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b9f-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b9f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b9f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1b9f-133">INPUTS</span></span>

### <span data-ttu-id="c1b9f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b9f-134">System.String</span></span>

## <span data-ttu-id="c1b9f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1b9f-135">OUTPUTS</span></span>

### <span data-ttu-id="c1b9f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b9f-136">System.Boolean</span></span>

## <span data-ttu-id="c1b9f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1b9f-137">NOTES</span></span>

## <span data-ttu-id="c1b9f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1b9f-138">RELATED LINKS</span></span>

[<span data-ttu-id="c1b9f-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c1b9f-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c1b9f-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c1b9f-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c1b9f-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c1b9f-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
