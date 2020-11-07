---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849205"
---
# <span data-ttu-id="6eadd-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6eadd-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6eadd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6eadd-102">SYNOPSIS</span></span>
<span data-ttu-id="6eadd-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="6eadd-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eadd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6eadd-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eadd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6eadd-105">DESCRIPTION</span></span>
<span data-ttu-id="6eadd-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6eadd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="6eadd-107">A **Get-AzureRmVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="6eadd-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6eadd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6eadd-108">EXAMPLES</span></span>

### <span data-ttu-id="6eadd-109">1: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="6eadd-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6eadd-110">A virtuális hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myGateway" néven.</span><span class="sxs-lookup"><span data-stu-id="6eadd-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6eadd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6eadd-111">PARAMETERS</span></span>

### <span data-ttu-id="6eadd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eadd-112">-DefaultProfile</span></span>
<span data-ttu-id="6eadd-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6eadd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eadd-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6eadd-114">-Name</span></span>
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

### <span data-ttu-id="6eadd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eadd-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6eadd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eadd-116">CommonParameters</span></span>
<span data-ttu-id="6eadd-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6eadd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eadd-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eadd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eadd-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eadd-119">INPUTS</span></span>

## <span data-ttu-id="6eadd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eadd-120">OUTPUTS</span></span>

### <span data-ttu-id="6eadd-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6eadd-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6eadd-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6eadd-122">NOTES</span></span>

## <span data-ttu-id="6eadd-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eadd-123">RELATED LINKS</span></span>

