---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841481"
---
# <span data-ttu-id="24b78-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24b78-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="24b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24b78-102">SYNOPSIS</span></span>
<span data-ttu-id="24b78-103">A virtuális hálózat összevonása.</span><span class="sxs-lookup"><span data-stu-id="24b78-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="24b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24b78-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24b78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24b78-105">DESCRIPTION</span></span>
<span data-ttu-id="24b78-106">A **Get-AzVirtualNetworkPeering** parancsmag a virtuális hálózat-összevonást kapja.</span><span class="sxs-lookup"><span data-stu-id="24b78-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="24b78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24b78-107">EXAMPLES</span></span>

### <span data-ttu-id="24b78-108">Példa 1: két virtuális hálózat közötti kapcsolatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="24b78-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="24b78-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24b78-109">PARAMETERS</span></span>

### <span data-ttu-id="24b78-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b78-110">-DefaultProfile</span></span>
<span data-ttu-id="24b78-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24b78-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b78-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24b78-112">-Name</span></span>
<span data-ttu-id="24b78-113">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24b78-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b78-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b78-114">-ResourceGroupName</span></span>
<span data-ttu-id="24b78-115">Annak az erőforráscsoport-névnek a neve, amelyhez a virtuális hálózat társközi tartozik.</span><span class="sxs-lookup"><span data-stu-id="24b78-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b78-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="24b78-116">-VirtualNetworkName</span></span>
<span data-ttu-id="24b78-117">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="24b78-117">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b78-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b78-118">CommonParameters</span></span>
<span data-ttu-id="24b78-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24b78-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b78-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b78-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b78-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24b78-121">INPUTS</span></span>

## <span data-ttu-id="24b78-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24b78-122">OUTPUTS</span></span>

### <span data-ttu-id="24b78-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24b78-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="24b78-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24b78-124">NOTES</span></span>

## <span data-ttu-id="24b78-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24b78-125">RELATED LINKS</span></span>

[<span data-ttu-id="24b78-126">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24b78-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="24b78-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24b78-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="24b78-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24b78-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


