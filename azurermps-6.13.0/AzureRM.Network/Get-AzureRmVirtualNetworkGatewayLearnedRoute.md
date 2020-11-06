---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 7c356a3f27959ccb0dd3160b8b984b304eac647d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495924"
---
# <span data-ttu-id="39fab-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="39fab-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="39fab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39fab-102">SYNOPSIS</span></span>
<span data-ttu-id="39fab-103">Az Azure virtuális hálózati átjáró által ismert útvonalak felsorolása</span><span class="sxs-lookup"><span data-stu-id="39fab-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39fab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39fab-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39fab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39fab-105">DESCRIPTION</span></span>
<span data-ttu-id="39fab-106">Az Azure virtuális hálózati átjáró által a különböző forrásokból megismert útvonalak enumerálása.</span><span class="sxs-lookup"><span data-stu-id="39fab-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="39fab-107">Ez a cikk a BGP-t, valamint a statikus útvonalakat is magába foglalja.</span><span class="sxs-lookup"><span data-stu-id="39fab-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="39fab-108">Példák</span><span class="sxs-lookup"><span data-stu-id="39fab-108">EXAMPLES</span></span>

### <span data-ttu-id="39fab-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39fab-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="39fab-110">A gatewayname nevű Azure Virtual Network Gateway resourceGroup-ös verziójában a következőt kell beolvasnia: az Azure Gateway tudja.</span><span class="sxs-lookup"><span data-stu-id="39fab-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="39fab-111">Az Azure virtuális hálózati átjáró ebben az esetben két statikus útvonalon (10.1.0.0/16 és 10.0.0.254/32), valamint egy, a BGP (10.0.0.0/16) (/16) útvonalon is ismert.</span><span class="sxs-lookup"><span data-stu-id="39fab-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="39fab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39fab-112">PARAMETERS</span></span>

### <span data-ttu-id="39fab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39fab-113">-AsJob</span></span>
<span data-ttu-id="39fab-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39fab-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39fab-115">-DefaultProfile</span></span>
<span data-ttu-id="39fab-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39fab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39fab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39fab-117">-ResourceGroupName</span></span>
<span data-ttu-id="39fab-118">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="39fab-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="39fab-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="39fab-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="39fab-120">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="39fab-120">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39fab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39fab-121">CommonParameters</span></span>
<span data-ttu-id="39fab-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39fab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39fab-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39fab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39fab-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39fab-124">INPUTS</span></span>

### <span data-ttu-id="39fab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="39fab-125">System.String</span></span>

## <span data-ttu-id="39fab-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39fab-126">OUTPUTS</span></span>

### <span data-ttu-id="39fab-127">Microsoft. Azure. commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="39fab-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="39fab-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39fab-128">NOTES</span></span>

## <span data-ttu-id="39fab-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39fab-129">RELATED LINKS</span></span>
