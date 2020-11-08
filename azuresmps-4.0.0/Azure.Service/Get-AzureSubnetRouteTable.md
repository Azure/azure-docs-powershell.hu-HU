---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015542"
---
# <span data-ttu-id="3b2e9-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3b2e9-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="3b2e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2e9-103">Egy alhálózat útválasztási táblázatát kapja.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="3b2e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b2e9-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b2e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b2e9-106">A **Get-AzureSubnetRouteTable** parancsmag az alhálózathoz társított útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="3b2e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b2e9-107">EXAMPLES</span></span>

### <span data-ttu-id="3b2e9-108">1. példa: az alhálózat útvonalait jeleníti meg</span><span class="sxs-lookup"><span data-stu-id="3b2e9-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="3b2e9-109">Ez a parancs megjeleníti a ContosoSubnet nevű alhálózattal társított útvonal-tábla útvonalait.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="3b2e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b2e9-110">PARAMETERS</span></span>

### <span data-ttu-id="3b2e9-111">– Részletes</span><span class="sxs-lookup"><span data-stu-id="3b2e9-111">-Detailed</span></span>
<span data-ttu-id="3b2e9-112">Azt jelzi, hogy ez a parancsmag az alhálózathoz társított útvonal táblában látható útvonalakat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2e9-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b2e9-113">-Profile</span></span>
<span data-ttu-id="3b2e9-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3b2e9-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2e9-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3b2e9-116">-SubnetName</span></span>
<span data-ttu-id="3b2e9-117">Azt az alhálózatot adja meg, amelyre a parancsmag az útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="3b2e9-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3b2e9-118">-VirtualNetworkName</span></span>
<span data-ttu-id="3b2e9-119">Megadja annak a virtuális hálózatnak a nevét, amely azt az alhálózatot tartalmazza, amelynek a parancsmagja az útválasztási táblázatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3b2e9-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="3b2e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2e9-120">CommonParameters</span></span>
<span data-ttu-id="3b2e9-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b2e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2e9-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2e9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2e9-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b2e9-123">INPUTS</span></span>

## <span data-ttu-id="3b2e9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b2e9-124">OUTPUTS</span></span>

## <span data-ttu-id="3b2e9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b2e9-125">NOTES</span></span>

## <span data-ttu-id="3b2e9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b2e9-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b2e9-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3b2e9-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="3b2e9-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3b2e9-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


