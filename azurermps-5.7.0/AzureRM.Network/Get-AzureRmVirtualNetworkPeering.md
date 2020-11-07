---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672632"
---
# <span data-ttu-id="1857e-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1857e-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="1857e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1857e-102">SYNOPSIS</span></span>
<span data-ttu-id="1857e-103">A virtuális hálózat összevonása.</span><span class="sxs-lookup"><span data-stu-id="1857e-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1857e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1857e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1857e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1857e-105">DESCRIPTION</span></span>
<span data-ttu-id="1857e-106">A **Get-AzureRmVirtualNetworkPeering** parancsmag a virtuális hálózat-összevonást kapja.</span><span class="sxs-lookup"><span data-stu-id="1857e-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="1857e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1857e-107">EXAMPLES</span></span>

### <span data-ttu-id="1857e-108">Példa 1: két virtuális hálózat közötti kapcsolatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="1857e-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="1857e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1857e-109">PARAMETERS</span></span>

### <span data-ttu-id="1857e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1857e-110">-DefaultProfile</span></span>
<span data-ttu-id="1857e-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1857e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1857e-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1857e-112">-Name</span></span>
<span data-ttu-id="1857e-113">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1857e-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="1857e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1857e-114">-ResourceGroupName</span></span>
<span data-ttu-id="1857e-115">Annak az erőforráscsoport-névnek a neve, amelyhez a virtuális hálózat társközi tartozik.</span><span class="sxs-lookup"><span data-stu-id="1857e-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="1857e-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1857e-116">-VirtualNetworkName</span></span>
<span data-ttu-id="1857e-117">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1857e-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1857e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1857e-118">CommonParameters</span></span>
<span data-ttu-id="1857e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1857e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1857e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1857e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1857e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1857e-121">INPUTS</span></span>

### <span data-ttu-id="1857e-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="1857e-122">None</span></span>
<span data-ttu-id="1857e-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1857e-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1857e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1857e-124">OUTPUTS</span></span>

### <span data-ttu-id="1857e-125">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1857e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="1857e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1857e-126">NOTES</span></span>

## <span data-ttu-id="1857e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1857e-127">RELATED LINKS</span></span>

[<span data-ttu-id="1857e-128">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1857e-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1857e-129">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1857e-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1857e-130">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1857e-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


