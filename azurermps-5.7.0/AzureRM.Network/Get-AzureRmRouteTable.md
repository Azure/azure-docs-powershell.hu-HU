---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 711d9848188cbdbaaeac9313680fd9fd70cb1f34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493749"
---
# <span data-ttu-id="651d1-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="651d1-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="651d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="651d1-102">SYNOPSIS</span></span>
<span data-ttu-id="651d1-103">Átveszi az útválasztási táblázatokat.</span><span class="sxs-lookup"><span data-stu-id="651d1-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="651d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="651d1-104">SYNTAX</span></span>

### <span data-ttu-id="651d1-105">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="651d1-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="651d1-106">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="651d1-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="651d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="651d1-107">DESCRIPTION</span></span>
<span data-ttu-id="651d1-108">A **Get-AzureRmRouteTable** parancsmag Azure Route-táblázatokat kap.</span><span class="sxs-lookup"><span data-stu-id="651d1-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="651d1-109">Beszerezhet egyetlen Route táblát, vagy beolvashatja az összes Route táblát egy erőforráscsoport vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="651d1-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="651d1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="651d1-110">EXAMPLES</span></span>

### <span data-ttu-id="651d1-111">Példa 1: útvonali táblázat beszerzése</span><span class="sxs-lookup"><span data-stu-id="651d1-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="651d1-112">Ez a parancs beilleszti a RouteTable01 nevű ResourceGroup11 nevű útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="651d1-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="651d1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="651d1-113">PARAMETERS</span></span>

### <span data-ttu-id="651d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651d1-114">-DefaultProfile</span></span>
<span data-ttu-id="651d1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="651d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="651d1-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="651d1-116">-ExpandResource</span></span>
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

### <span data-ttu-id="651d1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="651d1-117">-Name</span></span>
<span data-ttu-id="651d1-118">Annak az útvonal-táblázatnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="651d1-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="651d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="651d1-120">Annak a csoportnak a nevét adja meg, amely a parancsmag által beolvasott útválasztási táblákat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="651d1-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="651d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651d1-121">CommonParameters</span></span>
<span data-ttu-id="651d1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="651d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651d1-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651d1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651d1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="651d1-124">INPUTS</span></span>

### <span data-ttu-id="651d1-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="651d1-125">None</span></span>
<span data-ttu-id="651d1-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="651d1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="651d1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="651d1-127">OUTPUTS</span></span>

### <span data-ttu-id="651d1-128">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="651d1-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="651d1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="651d1-129">NOTES</span></span>

## <span data-ttu-id="651d1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="651d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="651d1-131">Új – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="651d1-131">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="651d1-132">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="651d1-132">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="651d1-133">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="651d1-133">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


