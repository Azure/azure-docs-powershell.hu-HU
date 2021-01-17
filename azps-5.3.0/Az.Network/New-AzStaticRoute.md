---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385390"
---
# <span data-ttu-id="72111-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="72111-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="72111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72111-102">SYNOPSIS</span></span>
<span data-ttu-id="72111-103">StatikusRoute-objektumot hoz létre, amelyet aztán hozzá lehet adni egy RoutingConfiguration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="72111-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="72111-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72111-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72111-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72111-105">DESCRIPTION</span></span>
<span data-ttu-id="72111-106">StatikusRoute-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="72111-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="72111-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72111-107">EXAMPLES</span></span>

### <span data-ttu-id="72111-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="72111-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="72111-109">A fenti parancs létrehoz egy StaticRoute-objektumot, amelyet aztán hozzá lehet adni egy RoutingConfiguration objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="72111-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="72111-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72111-110">PARAMETERS</span></span>

### <span data-ttu-id="72111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72111-111">-DefaultProfile</span></span>
<span data-ttu-id="72111-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72111-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72111-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72111-113">-AddressPrefix</span></span>
<span data-ttu-id="72111-114">Címelőtagok listája.</span><span class="sxs-lookup"><span data-stu-id="72111-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="72111-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72111-115">-Name</span></span>
<span data-ttu-id="72111-116">Az útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="72111-116">The route name.</span></span>

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

### <span data-ttu-id="72111-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="72111-117">-NextHopIpAddress</span></span>
<span data-ttu-id="72111-118">A következő ugrás ip-címe.</span><span class="sxs-lookup"><span data-stu-id="72111-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="72111-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72111-119">CommonParameters</span></span>
<span data-ttu-id="72111-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72111-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72111-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72111-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72111-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72111-122">INPUTS</span></span>

### <span data-ttu-id="72111-123">System.String</span><span class="sxs-lookup"><span data-stu-id="72111-123">System.String</span></span>

## <span data-ttu-id="72111-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72111-124">OUTPUTS</span></span>

### <span data-ttu-id="72111-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="72111-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="72111-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72111-126">NOTES</span></span>

## <span data-ttu-id="72111-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72111-127">RELATED LINKS</span></span>

[<span data-ttu-id="72111-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="72111-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
