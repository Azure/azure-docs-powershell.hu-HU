---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011379"
---
# <span data-ttu-id="e10c6-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e10c6-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e10c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e10c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e10c6-103">A virtuális hálózat összevonása.</span><span class="sxs-lookup"><span data-stu-id="e10c6-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="e10c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e10c6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e10c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e10c6-106">A **Get-AzVirtualNetworkPeering** parancsmag a virtuális hálózat-összevonást kapja.</span><span class="sxs-lookup"><span data-stu-id="e10c6-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="e10c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e10c6-107">EXAMPLES</span></span>

### <span data-ttu-id="e10c6-108">Példa 1: két virtuális hálózat közötti kapcsolatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e10c6-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="e10c6-109">2. példa: a virtuális hálózat minden nézetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="e10c6-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e10c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e10c6-110">PARAMETERS</span></span>

### <span data-ttu-id="e10c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10c6-111">-DefaultProfile</span></span>
<span data-ttu-id="e10c6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e10c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e10c6-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e10c6-113">-Name</span></span>
<span data-ttu-id="e10c6-114">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e10c6-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e10c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="e10c6-116">Annak az erőforráscsoport-névnek a neve, amelyhez a virtuális hálózat társközi tartozik.</span><span class="sxs-lookup"><span data-stu-id="e10c6-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="e10c6-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e10c6-117">-VirtualNetworkName</span></span>
<span data-ttu-id="e10c6-118">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e10c6-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e10c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10c6-119">CommonParameters</span></span>
<span data-ttu-id="e10c6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e10c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10c6-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e10c6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10c6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e10c6-122">INPUTS</span></span>

### <span data-ttu-id="e10c6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e10c6-123">System.String</span></span>

## <span data-ttu-id="e10c6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e10c6-124">OUTPUTS</span></span>

### <span data-ttu-id="e10c6-125">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e10c6-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e10c6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e10c6-126">NOTES</span></span>

## <span data-ttu-id="e10c6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e10c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="e10c6-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e10c6-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e10c6-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e10c6-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e10c6-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e10c6-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
