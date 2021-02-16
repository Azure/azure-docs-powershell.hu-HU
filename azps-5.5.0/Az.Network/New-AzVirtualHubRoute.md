---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160794"
---
# <span data-ttu-id="b75ba-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b75ba-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="b75ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b75ba-103">Létrehoz egy Azure Virtual Hub Route-objektumot.</span><span class="sxs-lookup"><span data-stu-id="b75ba-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b75ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b75ba-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b75ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b75ba-106">Létrehoz egy Azure Virtual Hub Route-objektumot.</span><span class="sxs-lookup"><span data-stu-id="b75ba-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b75ba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b75ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b75ba-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b75ba-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="b75ba-109">A fenti virtuális központi útvonalobjektumot hoz létre, amely része lehet a virtuális központi útvonaltáblának.</span><span class="sxs-lookup"><span data-stu-id="b75ba-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="b75ba-110">A virtuális központi útvonal egy memóriaobjektum, amely VirtualHubRouteTable-objektum létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="b75ba-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="b75ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b75ba-111">PARAMETERS</span></span>

### <span data-ttu-id="b75ba-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b75ba-112">-AddressPrefix</span></span>
<span data-ttu-id="b75ba-113">Címelőtagok listája.</span><span class="sxs-lookup"><span data-stu-id="b75ba-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75ba-114">-DefaultProfile</span></span>
<span data-ttu-id="b75ba-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b75ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75ba-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b75ba-116">-NextHopIpAddress</span></span>
<span data-ttu-id="b75ba-117">The Next Hop IpAddress.</span><span class="sxs-lookup"><span data-stu-id="b75ba-117">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75ba-118">CommonParameters</span></span>
<span data-ttu-id="b75ba-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75ba-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75ba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75ba-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b75ba-121">INPUTS</span></span>

### <span data-ttu-id="b75ba-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="b75ba-122">None</span></span>

## <span data-ttu-id="b75ba-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b75ba-123">OUTPUTS</span></span>

### <span data-ttu-id="b75ba-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b75ba-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="b75ba-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b75ba-125">NOTES</span></span>

## <span data-ttu-id="b75ba-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b75ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="b75ba-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b75ba-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
