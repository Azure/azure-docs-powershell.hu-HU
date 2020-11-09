---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303584"
---
# <span data-ttu-id="62903-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="62903-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62903-102">SYNOPSIS</span></span>
<span data-ttu-id="62903-103">Privát végpont frissítése</span><span class="sxs-lookup"><span data-stu-id="62903-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="62903-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62903-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62903-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62903-105">DESCRIPTION</span></span>
<span data-ttu-id="62903-106">A **set-AzPrivateEndpoint** parancsmag egy privát végpontot frissít.</span><span class="sxs-lookup"><span data-stu-id="62903-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="62903-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62903-107">EXAMPLES</span></span>

### <span data-ttu-id="62903-108">1: privát végpontot hoz létre, és egyik alhálózatát egy másikra cseréli.</span><span class="sxs-lookup"><span data-stu-id="62903-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="62903-109">Ez a példa létrehoz egy privát végpontot egy alhálózattal, majd a virtuális hálózat memóriában való megjelenítésével egy másik alhálózatra cseréli.</span><span class="sxs-lookup"><span data-stu-id="62903-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="62903-110">A rendszer ekkor a Set-PrivateEndpoint parancsmagot használja a módosított privát végpont-állapot írásához a szolgáltatás oldalán.</span><span class="sxs-lookup"><span data-stu-id="62903-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="62903-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62903-111">PARAMETERS</span></span>

### <span data-ttu-id="62903-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62903-112">-AsJob</span></span>
<span data-ttu-id="62903-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="62903-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62903-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62903-114">-DefaultProfile</span></span>
<span data-ttu-id="62903-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62903-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62903-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-116">-PrivateEndpoint</span></span>
<span data-ttu-id="62903-117">Egy privát végpont-objektumot ad meg, amely azt az államot jelenti, amelyhez a privát végpontot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="62903-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62903-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62903-118">CommonParameters</span></span>
<span data-ttu-id="62903-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62903-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62903-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62903-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62903-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62903-121">INPUTS</span></span>

### <span data-ttu-id="62903-122">Microsoft. Azure. commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="62903-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62903-123">OUTPUTS</span></span>

### <span data-ttu-id="62903-124">Microsoft. Azure. commands. Network. models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="62903-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62903-125">NOTES</span></span>

## <span data-ttu-id="62903-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62903-126">RELATED LINKS</span></span>

[<span data-ttu-id="62903-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="62903-128">Új – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="62903-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="62903-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


