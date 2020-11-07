---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837541"
---
# <span data-ttu-id="65b2d-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="65b2d-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="65b2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="65b2d-103">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="65b2d-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="65b2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65b2d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="65b2d-106">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="65b2d-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="65b2d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="65b2d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65b2d-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="65b2d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65b2d-109">PARAMETERS</span></span>

### <span data-ttu-id="65b2d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b2d-110">-DefaultProfile</span></span>
<span data-ttu-id="65b2d-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65b2d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65b2d-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65b2d-112">-Name</span></span>
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

### <span data-ttu-id="65b2d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b2d-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="65b2d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b2d-114">CommonParameters</span></span>
<span data-ttu-id="65b2d-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65b2d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b2d-116">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65b2d-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b2d-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b2d-117">INPUTS</span></span>

### <span data-ttu-id="65b2d-118">System. String</span><span class="sxs-lookup"><span data-stu-id="65b2d-118">System.String</span></span>

## <span data-ttu-id="65b2d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b2d-119">OUTPUTS</span></span>

### <span data-ttu-id="65b2d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="65b2d-120">System.String</span></span>

## <span data-ttu-id="65b2d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65b2d-121">NOTES</span></span>

## <span data-ttu-id="65b2d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65b2d-122">RELATED LINKS</span></span>

[<span data-ttu-id="65b2d-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="65b2d-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="65b2d-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="65b2d-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
