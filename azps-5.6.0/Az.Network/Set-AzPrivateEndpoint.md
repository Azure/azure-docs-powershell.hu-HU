---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016166"
---
# <span data-ttu-id="74d7b-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="74d7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="74d7b-103">Egy privát végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="74d7b-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="74d7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74d7b-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74d7b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="74d7b-106">A **Set-AzPrivateEndpoint** parancsmag frissíti a magánjellegű végpontot.</span><span class="sxs-lookup"><span data-stu-id="74d7b-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="74d7b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="74d7b-108">1: Privát végpontot hoz létre, és az egyik alhálózatát lecseréli egy másikra.</span><span class="sxs-lookup"><span data-stu-id="74d7b-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="74d7b-109">Ebben a példában létrehoz egy magánjellegű végpontot egy alhálózattal, majd a virtuális hálózat memóriában való ábrázolása alapján lecseréli egy másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="74d7b-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="74d7b-110">A Set-PrivateEndpoint ezt követően a módosított privát végpontállapotot a szolgáltatásoldalra írja.</span><span class="sxs-lookup"><span data-stu-id="74d7b-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="74d7b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74d7b-111">PARAMETERS</span></span>

### <span data-ttu-id="74d7b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74d7b-112">-AsJob</span></span>
<span data-ttu-id="74d7b-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74d7b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74d7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d7b-114">-DefaultProfile</span></span>
<span data-ttu-id="74d7b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74d7b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d7b-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-116">-PrivateEndpoint</span></span>
<span data-ttu-id="74d7b-117">Egy privát végpontobjektumot ad meg, amely azt az állapotot képviseli, amelyben a privát végpontot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="74d7b-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="74d7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d7b-118">CommonParameters</span></span>
<span data-ttu-id="74d7b-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d7b-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74d7b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d7b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74d7b-121">INPUTS</span></span>

### <span data-ttu-id="74d7b-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="74d7b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74d7b-123">OUTPUTS</span></span>

### <span data-ttu-id="74d7b-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="74d7b-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74d7b-125">NOTES</span></span>

## <span data-ttu-id="74d7b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74d7b-126">RELATED LINKS</span></span>

[<span data-ttu-id="74d7b-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="74d7b-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="74d7b-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74d7b-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


