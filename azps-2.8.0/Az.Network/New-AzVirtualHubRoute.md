---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837161"
---
# <span data-ttu-id="a0de7-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a0de7-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="a0de7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0de7-102">SYNOPSIS</span></span>
<span data-ttu-id="a0de7-103">Azure Virtual hub Route objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a0de7-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="a0de7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0de7-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0de7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0de7-105">DESCRIPTION</span></span>
<span data-ttu-id="a0de7-106">Azure Virtual hub Route objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a0de7-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="a0de7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0de7-107">EXAMPLES</span></span>

### <span data-ttu-id="a0de7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0de7-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="a0de7-109">A fenti létrehoz egy virtuális hub útvonal-objektumot, amely megtalálható a virtuális hub útvonali táblázatban.</span><span class="sxs-lookup"><span data-stu-id="a0de7-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="a0de7-110">A virtuális hub útvonala egy memóriabeli objektum, amely a VirtualHubRouteTable objektum létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="a0de7-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="a0de7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0de7-111">PARAMETERS</span></span>

### <span data-ttu-id="a0de7-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a0de7-112">-AddressPrefix</span></span>
<span data-ttu-id="a0de7-113">A cím előtagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a0de7-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="a0de7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0de7-114">-DefaultProfile</span></span>
<span data-ttu-id="a0de7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0de7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0de7-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0de7-116">-NextHopIpAddress</span></span>
<span data-ttu-id="a0de7-117">A következő ugrás az IP-címen.</span><span class="sxs-lookup"><span data-stu-id="a0de7-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="a0de7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0de7-118">CommonParameters</span></span>
<span data-ttu-id="a0de7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0de7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0de7-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0de7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0de7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0de7-121">INPUTS</span></span>

### <span data-ttu-id="a0de7-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0de7-122">None</span></span>

## <span data-ttu-id="a0de7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0de7-123">OUTPUTS</span></span>

### <span data-ttu-id="a0de7-124">Microsoft. Azure. commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a0de7-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="a0de7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0de7-125">NOTES</span></span>

## <span data-ttu-id="a0de7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0de7-126">RELATED LINKS</span></span>

[<span data-ttu-id="a0de7-127">Új – AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a0de7-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
