---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324095"
---
# <span data-ttu-id="43d0c-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="43d0c-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="43d0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="43d0c-103">Az Azure virtuális hálózati átjáró által tanult útvonalak listája</span><span class="sxs-lookup"><span data-stu-id="43d0c-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="43d0c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43d0c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d0c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="43d0c-106">Felsorolja az Azure virtuális hálózati átjáró által a különböző forrásokból tanult útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="43d0c-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="43d0c-107">Ide tartoznak a BGP-kapcsolaton keresztül tanult útvonalak, valamint a statikus útvonalak is.</span><span class="sxs-lookup"><span data-stu-id="43d0c-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="43d0c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43d0c-108">EXAMPLES</span></span>

### <span data-ttu-id="43d0c-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="43d0c-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="43d0c-110">Az Erőforráscsoport erőforráscsoportban az átjárónév nevű Azure virtuális hálózati átjáró esetében beolvassa az Azure-átjáró által ismert útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="43d0c-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="43d0c-111">Ebben az esetben az Azure virtuális hálózati átjárónak két statikus útvonala van (10.1.0.0/16 és 10.0.0.254/32), valamint egy BGP-en keresztül tanult útvonal (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="43d0c-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="43d0c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d0c-112">PARAMETERS</span></span>

### <span data-ttu-id="43d0c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43d0c-113">-AsJob</span></span>
<span data-ttu-id="43d0c-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43d0c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43d0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d0c-115">-DefaultProfile</span></span>
<span data-ttu-id="43d0c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43d0c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43d0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="43d0c-118">Virtuális hálózati átjáró erőforráscsoportja neve</span><span class="sxs-lookup"><span data-stu-id="43d0c-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="43d0c-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="43d0c-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="43d0c-120">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="43d0c-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="43d0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d0c-121">CommonParameters</span></span>
<span data-ttu-id="43d0c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d0c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43d0c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d0c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43d0c-124">INPUTS</span></span>

### <span data-ttu-id="43d0c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="43d0c-125">System.String</span></span>

## <span data-ttu-id="43d0c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43d0c-126">OUTPUTS</span></span>

### <span data-ttu-id="43d0c-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="43d0c-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="43d0c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43d0c-128">NOTES</span></span>

## <span data-ttu-id="43d0c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43d0c-129">RELATED LINKS</span></span>
