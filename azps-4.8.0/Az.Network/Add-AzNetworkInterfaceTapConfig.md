---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183062"
---
# <span data-ttu-id="457d1-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="457d1-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="457d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="457d1-102">SYNOPSIS</span></span>
<span data-ttu-id="457d1-103">Egy NetworkInterface társított TapConfiguration-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="457d1-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="457d1-104">Ez egy meglévő VirtualNetworkTap-erőforrásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="457d1-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="457d1-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="457d1-105">SYNTAX</span></span>

### <span data-ttu-id="457d1-106">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="457d1-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="457d1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="457d1-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="457d1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="457d1-108">DESCRIPTION</span></span>
<span data-ttu-id="457d1-109">Az **Add-AzNetworkInterfaceTapConfig** parancsmag egy NetworkInterface társított TapConfiguration-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="457d1-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="457d1-110">Ez egy meglévő VirtualNetworkTap-erőforrásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="457d1-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="457d1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="457d1-111">EXAMPLES</span></span>

### <span data-ttu-id="457d1-112">1. példa: TapConfiguration hozzáadása adott NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="457d1-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="457d1-113">Adja hozzá a TapConfiguration a sourceNic.</span><span class="sxs-lookup"><span data-stu-id="457d1-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="457d1-114">A sourceNic VM-ről érkező forgalmat a vVirtualNetworkTap-erőforrásban hivatkozott cél VM-re fogja tükrözni.</span><span class="sxs-lookup"><span data-stu-id="457d1-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="457d1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="457d1-115">PARAMETERS</span></span>

### <span data-ttu-id="457d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457d1-116">-DefaultProfile</span></span>
<span data-ttu-id="457d1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="457d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="457d1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="457d1-118">-Name</span></span>
<span data-ttu-id="457d1-119">A koppintás konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="457d1-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="457d1-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="457d1-120">-NetworkInterface</span></span>
<span data-ttu-id="457d1-121">A hálózati kapcsolat erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="457d1-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="457d1-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="457d1-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="457d1-123">A virtuális hálózat hivatkozása: érintse meg az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="457d1-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457d1-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="457d1-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="457d1-125">A virtuális hálózat hivatkozása: érintse meg az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="457d1-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="457d1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="457d1-126">-Confirm</span></span>
<span data-ttu-id="457d1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="457d1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="457d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="457d1-128">-WhatIf</span></span>
<span data-ttu-id="457d1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="457d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="457d1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="457d1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="457d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457d1-131">CommonParameters</span></span>
<span data-ttu-id="457d1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="457d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457d1-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457d1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457d1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="457d1-134">INPUTS</span></span>

### <span data-ttu-id="457d1-135">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="457d1-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="457d1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="457d1-136">System.String</span></span>

### <span data-ttu-id="457d1-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="457d1-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="457d1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="457d1-138">OUTPUTS</span></span>

### <span data-ttu-id="457d1-139">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="457d1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="457d1-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="457d1-140">NOTES</span></span>

## <span data-ttu-id="457d1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="457d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="457d1-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="457d1-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="457d1-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="457d1-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="457d1-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="457d1-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
