---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a9a9c8705307b7c9ec3e71a9278c29637c4afc3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670499"
---
# <span data-ttu-id="c3dd4-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3dd4-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="c3dd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dd4-103">Átveszi az útválasztási táblázatokat.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-103">Gets route tables.</span></span>

## <span data-ttu-id="c3dd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3dd4-104">SYNTAX</span></span>

### <span data-ttu-id="c3dd4-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3dd4-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3dd4-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="c3dd4-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3dd4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3dd4-107">DESCRIPTION</span></span>
<span data-ttu-id="c3dd4-108">A **Get-AzRouteTable** parancsmag Azure Route-táblázatokat kap.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="c3dd4-109">Beszerezhet egyetlen Route táblát, vagy beolvashatja az összes Route táblát egy erőforráscsoport vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="c3dd4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3dd4-110">EXAMPLES</span></span>

### <span data-ttu-id="c3dd4-111">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="c3dd4-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

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

<span data-ttu-id="c3dd4-112">Ez a parancs beilleszti a RouteTable01 nevű ResourceGroup11 nevű útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c3dd4-113">2. példa: a lista Route-táblái szűréssel</span><span class="sxs-lookup"><span data-stu-id="c3dd4-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

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

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="c3dd4-114">Ez a parancs minden olyan útválasztási táblát beolvas, amelynek a neve "RouteTable"-val kezdődik</span><span class="sxs-lookup"><span data-stu-id="c3dd4-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="c3dd4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3dd4-115">PARAMETERS</span></span>

### <span data-ttu-id="c3dd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dd4-116">-DefaultProfile</span></span>
<span data-ttu-id="c3dd4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3dd4-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c3dd4-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3dd4-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3dd4-119">-Name</span></span>
<span data-ttu-id="c3dd4-120">Annak az útvonal-táblázatnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c3dd4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3dd4-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3dd4-122">Annak a csoportnak a nevét adja meg, amely a parancsmag által beolvasott útválasztási táblákat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c3dd4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dd4-123">CommonParameters</span></span>
<span data-ttu-id="c3dd4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3dd4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dd4-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3dd4-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dd4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3dd4-126">INPUTS</span></span>

### <span data-ttu-id="c3dd4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c3dd4-127">System.String</span></span>

## <span data-ttu-id="c3dd4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3dd4-128">OUTPUTS</span></span>

### <span data-ttu-id="c3dd4-129">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3dd4-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c3dd4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3dd4-130">NOTES</span></span>

## <span data-ttu-id="c3dd4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3dd4-131">RELATED LINKS</span></span>

[<span data-ttu-id="c3dd4-132">Új – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3dd4-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="c3dd4-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3dd4-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="c3dd4-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3dd4-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


