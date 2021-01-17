---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381021"
---
# <span data-ttu-id="0ac6d-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="0ac6d-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="0ac6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac6d-103">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="0ac6d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ac6d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac6d-106">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="0ac6d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ac6d-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac6d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ac6d-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="0ac6d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-109">PARAMETERS</span></span>

### <span data-ttu-id="0ac6d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac6d-110">-DefaultProfile</span></span>
<span data-ttu-id="0ac6d-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ac6d-112">-Name</span><span class="sxs-lookup"><span data-stu-id="0ac6d-112">-Name</span></span>
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

### <span data-ttu-id="0ac6d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac6d-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0ac6d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac6d-114">CommonParameters</span></span>
<span data-ttu-id="0ac6d-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac6d-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac6d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac6d-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-117">INPUTS</span></span>

### <span data-ttu-id="0ac6d-118">System.String</span><span class="sxs-lookup"><span data-stu-id="0ac6d-118">System.String</span></span>

## <span data-ttu-id="0ac6d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac6d-119">OUTPUTS</span></span>

### <span data-ttu-id="0ac6d-120">System.String</span><span class="sxs-lookup"><span data-stu-id="0ac6d-120">System.String</span></span>

## <span data-ttu-id="0ac6d-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ac6d-121">NOTES</span></span>

## <span data-ttu-id="0ac6d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ac6d-122">RELATED LINKS</span></span>

[<span data-ttu-id="0ac6d-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="0ac6d-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="0ac6d-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="0ac6d-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
