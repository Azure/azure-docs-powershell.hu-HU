---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025170"
---
# <span data-ttu-id="1d1ed-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="1d1ed-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="1d1ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1ed-103">Létrehoz egy StaticRoute objektumot, amelyet azután hozzáadhat egy RoutingConfiguration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="1d1ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d1ed-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d1ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d1ed-105">DESCRIPTION</span></span>
<span data-ttu-id="1d1ed-106">StaticRoute objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="1d1ed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d1ed-107">EXAMPLES</span></span>

### <span data-ttu-id="1d1ed-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d1ed-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="1d1ed-109">A fenti parancs létrehoz egy StaticRoute objektumot, amelyet Ezután hozzáadhat a RoutingConfiguration-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="1d1ed-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d1ed-110">PARAMETERS</span></span>

### <span data-ttu-id="1d1ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1ed-111">-DefaultProfile</span></span>
<span data-ttu-id="1d1ed-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1ed-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1d1ed-113">-AddressPrefix</span></span>
<span data-ttu-id="1d1ed-114">A cím előtagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1ed-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d1ed-115">-Name</span></span>
<span data-ttu-id="1d1ed-116">Az útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1ed-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1d1ed-117">-NextHopIpAddress</span></span>
<span data-ttu-id="1d1ed-118">A következő ugrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1ed-119">CommonParameters</span></span>
<span data-ttu-id="1d1ed-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d1ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1ed-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d1ed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1ed-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d1ed-122">INPUTS</span></span>

### <span data-ttu-id="1d1ed-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1d1ed-123">System.String</span></span>

## <span data-ttu-id="1d1ed-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d1ed-124">OUTPUTS</span></span>

### <span data-ttu-id="1d1ed-125">Microsoft. Azure. commands. Network. models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="1d1ed-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="1d1ed-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d1ed-126">NOTES</span></span>

## <span data-ttu-id="1d1ed-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d1ed-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d1ed-128">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1ed-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
