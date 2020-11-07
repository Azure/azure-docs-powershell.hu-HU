---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841518"
---
# <span data-ttu-id="b5405-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5405-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="b5405-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5405-102">SYNOPSIS</span></span>
<span data-ttu-id="b5405-103">Átveszi az útválasztási táblázatokat.</span><span class="sxs-lookup"><span data-stu-id="b5405-103">Gets route tables.</span></span>

## <span data-ttu-id="b5405-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5405-104">SYNTAX</span></span>

### <span data-ttu-id="b5405-105">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="b5405-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5405-106">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="b5405-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5405-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5405-107">DESCRIPTION</span></span>
<span data-ttu-id="b5405-108">A **Get-AzRouteTable** parancsmag Azure Route-táblázatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b5405-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="b5405-109">Beszerezhet egyetlen Route táblát, vagy beolvashatja az összes Route táblát egy erőforráscsoport vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b5405-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="b5405-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5405-110">EXAMPLES</span></span>

### <span data-ttu-id="b5405-111">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5405-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="b5405-112">Ez a parancs beilleszti a RouteTable01 nevű ResourceGroup11 nevű útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b5405-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="b5405-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5405-113">PARAMETERS</span></span>

### <span data-ttu-id="b5405-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5405-114">-DefaultProfile</span></span>
<span data-ttu-id="b5405-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5405-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5405-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b5405-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5405-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5405-117">-Name</span></span>
<span data-ttu-id="b5405-118">Annak az útvonal-táblázatnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b5405-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5405-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5405-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5405-120">Annak a csoportnak a nevét adja meg, amely a parancsmag által beolvasott útválasztási táblákat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5405-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5405-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5405-121">CommonParameters</span></span>
<span data-ttu-id="b5405-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5405-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5405-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5405-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5405-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5405-124">INPUTS</span></span>

## <span data-ttu-id="b5405-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5405-125">OUTPUTS</span></span>

### <span data-ttu-id="b5405-126">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5405-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b5405-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5405-127">NOTES</span></span>

## <span data-ttu-id="b5405-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5405-128">RELATED LINKS</span></span>

[<span data-ttu-id="b5405-129">Új – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5405-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="b5405-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5405-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="b5405-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5405-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


