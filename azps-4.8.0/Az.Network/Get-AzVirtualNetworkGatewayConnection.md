---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181031"
---
# <span data-ttu-id="58445-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="58445-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="58445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58445-102">SYNOPSIS</span></span>
<span data-ttu-id="58445-103">Virtuális hálózati átjáró csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="58445-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="58445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58445-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="58445-105">DESCRIPTION</span></span>
<span data-ttu-id="58445-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="58445-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="58445-107">A **Get-AzVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="58445-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="58445-108">Ha a **Get-AzVirtualNetworkGatewayConnection** parancsmagot a-name paraméter megadása nélkül bocsátja ki, akkor a kimenet nem jeleníti meg a ConnectionStatus és a SharedKey részleteket.</span><span class="sxs-lookup"><span data-stu-id="58445-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="58445-109">Példák</span><span class="sxs-lookup"><span data-stu-id="58445-109">EXAMPLES</span></span>

### <span data-ttu-id="58445-110">1: virtuális hálózati átjáró kapcsolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="58445-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="58445-111">A virtuális hálózati átjáró kapcsolat objektumát adja eredményül az "myRG" erőforráscsoporthoz tartozó "myTunnel" néven.</span><span class="sxs-lookup"><span data-stu-id="58445-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="58445-112">2: a virtuális hálózati átjáró-kapcsolatok beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="58445-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="58445-113">Az összes olyan virtuális hálózati átjáró-kapcsolat értékét jeleníti meg, amely "myTunnel"-val kezdődik a "myRG" erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="58445-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="58445-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58445-114">PARAMETERS</span></span>

### <span data-ttu-id="58445-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58445-115">-DefaultProfile</span></span>
<span data-ttu-id="58445-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58445-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58445-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58445-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="58445-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58445-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="58445-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58445-119">CommonParameters</span></span>
<span data-ttu-id="58445-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58445-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58445-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="58445-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58445-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58445-122">INPUTS</span></span>

### <span data-ttu-id="58445-123">System. String</span><span class="sxs-lookup"><span data-stu-id="58445-123">System.String</span></span>

## <span data-ttu-id="58445-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58445-124">OUTPUTS</span></span>

### <span data-ttu-id="58445-125">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="58445-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="58445-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58445-126">NOTES</span></span>

## <span data-ttu-id="58445-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58445-127">RELATED LINKS</span></span>

[<span data-ttu-id="58445-128">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="58445-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="58445-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="58445-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="58445-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="58445-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
