---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3d58e2f9fbd62826084df329cd7047a293ef0291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497792"
---
# <span data-ttu-id="8146d-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8146d-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8146d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8146d-102">SYNOPSIS</span></span>
<span data-ttu-id="8146d-103">Virtuális hálózati átjáró csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="8146d-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8146d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8146d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8146d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8146d-105">DESCRIPTION</span></span>
<span data-ttu-id="8146d-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="8146d-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="8146d-107">A **Get-AzureRmVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="8146d-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8146d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8146d-108">EXAMPLES</span></span>

### <span data-ttu-id="8146d-109">1: virtuális hálózati átjáró kapcsolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="8146d-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="8146d-110">A virtuális hálózati átjáró kapcsolat objektumát adja eredményül az "myRG" erőforráscsoporthoz tartozó "myTunnel" néven.</span><span class="sxs-lookup"><span data-stu-id="8146d-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="8146d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8146d-111">PARAMETERS</span></span>

### <span data-ttu-id="8146d-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8146d-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8146d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8146d-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8146d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8146d-114">-DefaultProfile</span></span>
<span data-ttu-id="8146d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8146d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8146d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8146d-116">CommonParameters</span></span>
<span data-ttu-id="8146d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8146d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8146d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8146d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8146d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8146d-119">INPUTS</span></span>

## <span data-ttu-id="8146d-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8146d-120">OUTPUTS</span></span>

### <span data-ttu-id="8146d-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8146d-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8146d-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8146d-122">NOTES</span></span>

## <span data-ttu-id="8146d-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8146d-123">RELATED LINKS</span></span>

