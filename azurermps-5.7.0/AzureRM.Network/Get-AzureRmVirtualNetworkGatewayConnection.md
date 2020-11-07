---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b4a6ae7db1221a2dee8a0bd5343ad78ed88a0abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672732"
---
# <span data-ttu-id="0ffad-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ffad-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ffad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ffad-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffad-103">Virtuális hálózati átjáró csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="0ffad-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ffad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ffad-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ffad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ffad-105">DESCRIPTION</span></span>
<span data-ttu-id="0ffad-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="0ffad-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="0ffad-107">A **Get-AzureRmVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="0ffad-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0ffad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0ffad-108">EXAMPLES</span></span>

### <span data-ttu-id="0ffad-109">1: virtuális hálózati átjáró kapcsolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ffad-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="0ffad-110">A virtuális hálózati átjáró kapcsolat objektumát adja eredményül az "myRG" erőforráscsoporthoz tartozó "myTunnel" néven.</span><span class="sxs-lookup"><span data-stu-id="0ffad-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="0ffad-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ffad-111">PARAMETERS</span></span>

### <span data-ttu-id="0ffad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffad-112">-DefaultProfile</span></span>
<span data-ttu-id="0ffad-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ffad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ffad-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ffad-114">-Name</span></span>
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

### <span data-ttu-id="0ffad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffad-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0ffad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffad-116">CommonParameters</span></span>
<span data-ttu-id="0ffad-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ffad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffad-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ffad-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffad-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ffad-119">INPUTS</span></span>

### <span data-ttu-id="0ffad-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ffad-120">None</span></span>
<span data-ttu-id="0ffad-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0ffad-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ffad-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ffad-122">OUTPUTS</span></span>

### <span data-ttu-id="0ffad-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ffad-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ffad-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ffad-124">NOTES</span></span>

## <span data-ttu-id="0ffad-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ffad-125">RELATED LINKS</span></span>

