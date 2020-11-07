---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841493"
---
# <span data-ttu-id="ae75a-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae75a-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ae75a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae75a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae75a-103">Virtuális hálózati átjáró csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="ae75a-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="ae75a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae75a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae75a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae75a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae75a-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="ae75a-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="ae75a-107">A **Get-AzVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="ae75a-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ae75a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ae75a-108">EXAMPLES</span></span>

### <span data-ttu-id="ae75a-109">1: virtuális hálózati átjáró kapcsolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ae75a-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ae75a-110">A virtuális hálózati átjáró kapcsolat objektumát adja eredményül az "myRG" erőforráscsoporthoz tartozó "myTunnel" néven.</span><span class="sxs-lookup"><span data-stu-id="ae75a-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ae75a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae75a-111">PARAMETERS</span></span>

### <span data-ttu-id="ae75a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae75a-112">-DefaultProfile</span></span>
<span data-ttu-id="ae75a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae75a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae75a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae75a-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae75a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae75a-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ae75a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae75a-116">CommonParameters</span></span>
<span data-ttu-id="ae75a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae75a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae75a-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae75a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae75a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae75a-119">INPUTS</span></span>

## <span data-ttu-id="ae75a-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae75a-120">OUTPUTS</span></span>

### <span data-ttu-id="ae75a-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae75a-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ae75a-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae75a-122">NOTES</span></span>

## <span data-ttu-id="ae75a-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae75a-123">RELATED LINKS</span></span>

