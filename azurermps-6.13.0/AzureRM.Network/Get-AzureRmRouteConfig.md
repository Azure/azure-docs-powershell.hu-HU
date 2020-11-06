---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495075"
---
# <span data-ttu-id="4add0-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4add0-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="4add0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4add0-102">SYNOPSIS</span></span>
<span data-ttu-id="4add0-103">Útvonal-táblázatból kapja az útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="4add0-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4add0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4add0-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4add0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4add0-105">DESCRIPTION</span></span>
<span data-ttu-id="4add0-106">A **Get-AzureRmRouteConfig** parancsmag az Azure Route-táblázatokból származó útvonalakat kapja.</span><span class="sxs-lookup"><span data-stu-id="4add0-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="4add0-107">Az útvonalat név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="4add0-107">You can specify a route by name.</span></span>

## <span data-ttu-id="4add0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4add0-108">EXAMPLES</span></span>

### <span data-ttu-id="4add0-109">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="4add0-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="4add0-110">Ez a parancs a **Get-AzureRmRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="4add0-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="4add0-111">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="4add0-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4add0-112">Az aktuális parancsmag a Route07 nevű útvonalat kapja a RouteTable01 nevű Route táblában.</span><span class="sxs-lookup"><span data-stu-id="4add0-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="4add0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4add0-113">PARAMETERS</span></span>

### <span data-ttu-id="4add0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4add0-114">-DefaultProfile</span></span>
<span data-ttu-id="4add0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4add0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4add0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4add0-116">-Name</span></span>
<span data-ttu-id="4add0-117">Itt adhatja meg annak az útvonalnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4add0-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4add0-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4add0-118">-RouteTable</span></span>
<span data-ttu-id="4add0-119">Annak az útvonalnak a táblázatát adja meg, amelyből a parancsmag útvonalait kapja.</span><span class="sxs-lookup"><span data-stu-id="4add0-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="4add0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4add0-120">CommonParameters</span></span>
<span data-ttu-id="4add0-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4add0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4add0-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4add0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4add0-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4add0-123">INPUTS</span></span>

### <span data-ttu-id="4add0-124">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4add0-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4add0-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4add0-125">OUTPUTS</span></span>

### <span data-ttu-id="4add0-126">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="4add0-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="4add0-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4add0-127">NOTES</span></span>

## <span data-ttu-id="4add0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4add0-128">RELATED LINKS</span></span>

[<span data-ttu-id="4add0-129">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4add0-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="4add0-130">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4add0-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="4add0-131">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4add0-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="4add0-132">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4add0-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="4add0-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4add0-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


