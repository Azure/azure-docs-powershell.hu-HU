---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841533"
---
# <span data-ttu-id="cf969-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cf969-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="cf969-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf969-102">SYNOPSIS</span></span>
<span data-ttu-id="cf969-103">Útvonal-táblázatból kapja az útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="cf969-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="cf969-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf969-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf969-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf969-105">DESCRIPTION</span></span>
<span data-ttu-id="cf969-106">A **Get-AzRouteConfig** parancsmag az Azure Route-táblázatokból származó útvonalakat kapja.</span><span class="sxs-lookup"><span data-stu-id="cf969-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="cf969-107">Az útvonalat név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="cf969-107">You can specify a route by name.</span></span>

## <span data-ttu-id="cf969-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cf969-108">EXAMPLES</span></span>

### <span data-ttu-id="cf969-109">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="cf969-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="cf969-110">Ez a parancs a **Get-AzRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="cf969-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="cf969-111">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="cf969-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cf969-112">Az aktuális parancsmag a Route07 nevű útvonalat kapja a RouteTable01 nevű Route táblában.</span><span class="sxs-lookup"><span data-stu-id="cf969-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="cf969-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf969-113">PARAMETERS</span></span>

### <span data-ttu-id="cf969-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf969-114">-DefaultProfile</span></span>
<span data-ttu-id="cf969-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf969-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf969-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf969-116">-Name</span></span>
<span data-ttu-id="cf969-117">Itt adhatja meg annak az útvonalnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="cf969-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf969-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="cf969-118">-RouteTable</span></span>
<span data-ttu-id="cf969-119">Annak az útvonalnak a táblázatát adja meg, amelyből a parancsmag útvonalait kapja.</span><span class="sxs-lookup"><span data-stu-id="cf969-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf969-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf969-120">CommonParameters</span></span>
<span data-ttu-id="cf969-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf969-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf969-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf969-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf969-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf969-123">INPUTS</span></span>

### <span data-ttu-id="cf969-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf969-124">PSRouteTable</span></span>
<span data-ttu-id="cf969-125">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf969-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="cf969-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf969-126">OUTPUTS</span></span>

### <span data-ttu-id="cf969-127">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="cf969-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="cf969-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf969-128">NOTES</span></span>

## <span data-ttu-id="cf969-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf969-129">RELATED LINKS</span></span>

[<span data-ttu-id="cf969-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cf969-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="cf969-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf969-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="cf969-132">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cf969-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="cf969-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cf969-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="cf969-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cf969-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


