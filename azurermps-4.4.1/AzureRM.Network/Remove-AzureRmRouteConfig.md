---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504039"
---
# <span data-ttu-id="c5bc2-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c5bc2-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c5bc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bc2-103">Egy útvonal eltávolítása az útvonal-táblázatból.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5bc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5bc2-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5bc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bc2-106">A **Remove-AzureRmRouteConfig** parancsmag az Azure Route-táblázatból távolítja el az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="c5bc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bc2-108">1. példa: útvonal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c5bc2-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="c5bc2-109">Ez a parancs a **Get-AzureRmRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="c5bc2-110">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5bc2-111">Az aktuális parancsmag eltávolítja a Route02 nevű útvonalat, és az eredményt átadja a **set-AzureRmRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="c5bc2-112">A táblázat már nem tartalmazza a Route02 nevű útvonalat.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="c5bc2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5bc2-113">PARAMETERS</span></span>

### <span data-ttu-id="c5bc2-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5bc2-114">-Name</span></span>
<span data-ttu-id="c5bc2-115">A parancsmag által eltávolított útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-115">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5bc2-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c5bc2-116">-RouteTable</span></span>
<span data-ttu-id="c5bc2-117">Annak az útvonalnak a táblázatát adja meg, amely a parancsmag által törölt útvonalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bc2-118">-DefaultProfile</span></span>
<span data-ttu-id="c5bc2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bc2-120">CommonParameters</span></span>
<span data-ttu-id="c5bc2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5bc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bc2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bc2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bc2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5bc2-123">INPUTS</span></span>

### <span data-ttu-id="c5bc2-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c5bc2-124">PSRouteTable</span></span>
<span data-ttu-id="c5bc2-125">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c5bc2-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c5bc2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5bc2-126">OUTPUTS</span></span>

### <span data-ttu-id="c5bc2-127">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c5bc2-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c5bc2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5bc2-128">NOTES</span></span>

## <span data-ttu-id="c5bc2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5bc2-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5bc2-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c5bc2-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="c5bc2-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c5bc2-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="c5bc2-132">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c5bc2-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="c5bc2-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c5bc2-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


