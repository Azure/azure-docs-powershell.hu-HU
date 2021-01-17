---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369346"
---
# <span data-ttu-id="80596-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="80596-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="80596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80596-102">SYNOPSIS</span></span>
<span data-ttu-id="80596-103">Útvonalakat kap egy útvonaltáblából.</span><span class="sxs-lookup"><span data-stu-id="80596-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="80596-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80596-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80596-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80596-105">DESCRIPTION</span></span>
<span data-ttu-id="80596-106">A **Get-AzRouteConfig** parancsmag útvonalakat kap egy Azure-útvonaltáblából.</span><span class="sxs-lookup"><span data-stu-id="80596-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="80596-107">Az útvonalat név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="80596-107">You can specify a route by name.</span></span>

## <span data-ttu-id="80596-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80596-108">EXAMPLES</span></span>

### <span data-ttu-id="80596-109">1. példa: Útvonaltábla lekérte</span><span class="sxs-lookup"><span data-stu-id="80596-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="80596-110">Ez a parancs a RouteTable01 nevű útvonaltáblát a **Get-AzRouteTable** parancsmaggal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80596-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="80596-111">A parancs a folyamat műveleti operátorával átadja a táblát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="80596-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80596-112">Az aktuális parancsmag a Route07 nevű útvonalat kapja meg a RouteTable01 nevű útválasztási táblában.</span><span class="sxs-lookup"><span data-stu-id="80596-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="80596-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80596-113">PARAMETERS</span></span>

### <span data-ttu-id="80596-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80596-114">-DefaultProfile</span></span>
<span data-ttu-id="80596-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80596-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80596-116">-Name</span><span class="sxs-lookup"><span data-stu-id="80596-116">-Name</span></span>
<span data-ttu-id="80596-117">A parancsmag által lekért útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="80596-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="80596-118">-RouteTable</span></span>
<span data-ttu-id="80596-119">Azt az útvonaltáblát adja meg, amelyből a parancsmag útvonalakat kap.</span><span class="sxs-lookup"><span data-stu-id="80596-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80596-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80596-120">CommonParameters</span></span>
<span data-ttu-id="80596-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80596-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80596-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80596-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80596-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80596-123">INPUTS</span></span>

### <span data-ttu-id="80596-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="80596-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="80596-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80596-125">OUTPUTS</span></span>

### <span data-ttu-id="80596-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="80596-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="80596-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80596-127">NOTES</span></span>

## <span data-ttu-id="80596-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80596-128">RELATED LINKS</span></span>

[<span data-ttu-id="80596-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="80596-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="80596-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="80596-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="80596-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="80596-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="80596-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="80596-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="80596-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="80596-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


