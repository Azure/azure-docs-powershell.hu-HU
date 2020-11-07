---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 195ff0f8da8af5408f9b7ad2bffdd35507b10d1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837294"
---
# <span data-ttu-id="4541e-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4541e-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="4541e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4541e-102">SYNOPSIS</span></span>
<span data-ttu-id="4541e-103">Útvonal-táblázatból kapja az útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="4541e-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="4541e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4541e-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4541e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4541e-105">DESCRIPTION</span></span>
<span data-ttu-id="4541e-106">A **Get-AzRouteConfig** parancsmag az Azure Route-táblázatokból származó útvonalakat kapja.</span><span class="sxs-lookup"><span data-stu-id="4541e-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="4541e-107">Az útvonalat név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="4541e-107">You can specify a route by name.</span></span>

## <span data-ttu-id="4541e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4541e-108">EXAMPLES</span></span>

### <span data-ttu-id="4541e-109">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="4541e-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="4541e-110">Ez a parancs a **Get-AzRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="4541e-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="4541e-111">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="4541e-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4541e-112">Az aktuális parancsmag a Route07 nevű útvonalat kapja a RouteTable01 nevű Route táblában.</span><span class="sxs-lookup"><span data-stu-id="4541e-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="4541e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4541e-113">PARAMETERS</span></span>

### <span data-ttu-id="4541e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4541e-114">-DefaultProfile</span></span>
<span data-ttu-id="4541e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4541e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4541e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4541e-116">-Name</span></span>
<span data-ttu-id="4541e-117">Itt adhatja meg annak az útvonalnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4541e-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4541e-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4541e-118">-RouteTable</span></span>
<span data-ttu-id="4541e-119">Annak az útvonalnak a táblázatát adja meg, amelyből a parancsmag útvonalait kapja.</span><span class="sxs-lookup"><span data-stu-id="4541e-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="4541e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4541e-120">CommonParameters</span></span>
<span data-ttu-id="4541e-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4541e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4541e-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4541e-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4541e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4541e-123">INPUTS</span></span>

### <span data-ttu-id="4541e-124">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4541e-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4541e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4541e-125">OUTPUTS</span></span>

### <span data-ttu-id="4541e-126">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="4541e-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="4541e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4541e-127">NOTES</span></span>

## <span data-ttu-id="4541e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4541e-128">RELATED LINKS</span></span>

[<span data-ttu-id="4541e-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4541e-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="4541e-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="4541e-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="4541e-131">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4541e-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="4541e-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4541e-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="4541e-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4541e-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


