---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348054"
---
# <span data-ttu-id="9769b-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9769b-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9769b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9769b-102">SYNOPSIS</span></span>
<span data-ttu-id="9769b-103">Virtuális hálózati átjárókapcsolatot létesít</span><span class="sxs-lookup"><span data-stu-id="9769b-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="9769b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9769b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9769b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9769b-105">DESCRIPTION</span></span>
<span data-ttu-id="9769b-106">A virtuális hálózati átjáró kapcsolata az Az Azure virtuális hálózati átjáróhoz csatlakoztatott IPsec-csatornát (Site-to-Site vagy Vnet-to-Vnet) képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="9769b-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="9769b-107">A **Get-AzVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja vissza a Név és az Erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="9769b-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="9769b-108">Ha a **Get-AzVirtualNetworkGatewayConnection** parancsmagot a -Name paraméter megadása nélkül bocsátotta ki, a kimenet nem fogja tartalmazni a ConnectionStatus és a SharedKey adatait.</span><span class="sxs-lookup"><span data-stu-id="9769b-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="9769b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9769b-109">EXAMPLES</span></span>

### <span data-ttu-id="9769b-110">1: Virtuális hálózati átjáró csatlakoztatása</span><span class="sxs-lookup"><span data-stu-id="9769b-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="9769b-111">A virtuális hálózati átjáró kapcsolatának "myTunnel" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="9769b-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="9769b-112">2: Az összes virtuális hálózati átjárókapcsolat behozása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="9769b-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="9769b-113">Visszaadja a "myTunnel" kezdetű virtuális hálózati átjárókapcsolatokat a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="9769b-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="9769b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9769b-114">PARAMETERS</span></span>

### <span data-ttu-id="9769b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9769b-115">-DefaultProfile</span></span>
<span data-ttu-id="9769b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9769b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9769b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9769b-117">-Name</span></span>
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

### <span data-ttu-id="9769b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9769b-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9769b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9769b-119">CommonParameters</span></span>
<span data-ttu-id="9769b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9769b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9769b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9769b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9769b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9769b-122">INPUTS</span></span>

### <span data-ttu-id="9769b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9769b-123">System.String</span></span>

## <span data-ttu-id="9769b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9769b-124">OUTPUTS</span></span>

### <span data-ttu-id="9769b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9769b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9769b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9769b-126">NOTES</span></span>

## <span data-ttu-id="9769b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9769b-127">RELATED LINKS</span></span>

[<span data-ttu-id="9769b-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9769b-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9769b-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9769b-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9769b-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9769b-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
