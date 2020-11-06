---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500191"
---
# <span data-ttu-id="e1d5d-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e1d5d-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="e1d5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d5d-103">Azure Virtual hub Route objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e1d5d-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1d5d-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d5d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d5d-106">Azure Virtual hub Route objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e1d5d-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="e1d5d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1d5d-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d5d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1d5d-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="e1d5d-109">A fenti létrehoz egy virtuális hub útvonal-objektumot, amely megtalálható a virtuális hub útvonali táblázatban.</span><span class="sxs-lookup"><span data-stu-id="e1d5d-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="e1d5d-110">A virtuális hub útvonala egy memóriabeli objektum, amely a VirtualHubRouteTable objektum létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="e1d5d-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="e1d5d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1d5d-111">PARAMETERS</span></span>

### <span data-ttu-id="e1d5d-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e1d5d-112">-AddressPrefix</span></span>
<span data-ttu-id="e1d5d-113">A cím előtagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="e1d5d-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="e1d5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d5d-114">-DefaultProfile</span></span>
<span data-ttu-id="e1d5d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1d5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d5d-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1d5d-116">-NextHopIpAddress</span></span>
<span data-ttu-id="e1d5d-117">A következő ugrás az IP-címen.</span><span class="sxs-lookup"><span data-stu-id="e1d5d-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="e1d5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d5d-118">CommonParameters</span></span>
<span data-ttu-id="e1d5d-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1d5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d5d-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d5d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d5d-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1d5d-121">INPUTS</span></span>

### <span data-ttu-id="e1d5d-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1d5d-122">None</span></span>

## <span data-ttu-id="e1d5d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1d5d-123">OUTPUTS</span></span>

### <span data-ttu-id="e1d5d-124">Microsoft. Azure. commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e1d5d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="e1d5d-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1d5d-125">NOTES</span></span>

## <span data-ttu-id="e1d5d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1d5d-126">RELATED LINKS</span></span>
