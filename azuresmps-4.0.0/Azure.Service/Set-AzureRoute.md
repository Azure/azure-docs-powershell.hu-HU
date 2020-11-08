---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015823"
---
# <span data-ttu-id="ffe7a-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="ffe7a-101">Set-AzureRoute</span></span>

## <span data-ttu-id="ffe7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffe7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe7a-103">Útvonalat hoz létre az útvonal-táblában.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="ffe7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffe7a-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ffe7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffe7a-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe7a-106">A **set-AzureRoute** parancsmag útvonalat hoz létre egy útvonal-táblában.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="ffe7a-107">Az új útvonal szinte azonnal életbe lép az útválasztási táblázathoz társított virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="ffe7a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ffe7a-108">EXAMPLES</span></span>

### <span data-ttu-id="ffe7a-109">Példa 1: virtuális készülék felvétele következő ugrási útvonalon</span><span class="sxs-lookup"><span data-stu-id="ffe7a-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="ffe7a-110">A parancs létrehoz egy ApplianceRouteTable nevű útvonalkártya-táblázatot a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="ffe7a-111">A parancs átadja az útválasztási táblázatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="ffe7a-112">Az aktuális parancsmag hozzáadja a ApplianceRoute03 nevű útvonalat, amely a következő ugrás típusú VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="ffe7a-113">A parancs a következő ugrási IP-címet és az útvonalhoz tartozó cím előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="ffe7a-114">2. példa: az Internet következő ugrási útvonalának felvétele</span><span class="sxs-lookup"><span data-stu-id="ffe7a-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="ffe7a-115">Ez a parancs a ApplianceRouteTable nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="ffe7a-116">A parancs átadja az útválasztási táblázatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="ffe7a-117">Az aktuális parancsmag hozzáadja a InternetRoute nevű útvonalat, amely egy internetes következő ugrás típusú.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="ffe7a-118">A parancs az útvonalhoz tartozó cím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="ffe7a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffe7a-119">PARAMETERS</span></span>

### <span data-ttu-id="ffe7a-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ffe7a-120">-AddressPrefix</span></span>
<span data-ttu-id="ffe7a-121">Az új útvonalhoz tartozó cím előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="ffe7a-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffe7a-122">-NextHopIpAddress</span></span>
<span data-ttu-id="ffe7a-123">Annak a készüléknek az IP-címét adja meg, amely az útvonalat használó forgalom következő ugrása.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="ffe7a-124">Ezt az értéket csak akkor adja meg, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="ffe7a-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="ffe7a-125">-NextHopType</span></span>
<span data-ttu-id="ffe7a-126">Az útvonalat használó forgalom következő ugrási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="ffe7a-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ffe7a-127">Valid values are:</span></span> 

- <span data-ttu-id="ffe7a-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="ffe7a-128">VPNGateway</span></span>
- <span data-ttu-id="ffe7a-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="ffe7a-129">VNETLocal</span></span>
- <span data-ttu-id="ffe7a-130">Internet</span><span class="sxs-lookup"><span data-stu-id="ffe7a-130">Internet</span></span>
- <span data-ttu-id="ffe7a-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ffe7a-131">VirtualAppliance</span></span>
- <span data-ttu-id="ffe7a-132">NULL</span><span class="sxs-lookup"><span data-stu-id="ffe7a-132">Null</span></span>

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

### <span data-ttu-id="ffe7a-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="ffe7a-133">-Profile</span></span>
<span data-ttu-id="ffe7a-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ffe7a-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffe7a-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="ffe7a-136">-RouteName</span></span>
<span data-ttu-id="ffe7a-137">A parancsmag által hozzáadott új útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ffe7a-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ffe7a-138">-RouteTable</span></span>
<span data-ttu-id="ffe7a-139">Annak az útvonalnak a táblázatát adja meg, amelyre a parancsmag hozzáadja az új útvonalat.</span><span class="sxs-lookup"><span data-stu-id="ffe7a-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe7a-140">CommonParameters</span></span>
<span data-ttu-id="ffe7a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffe7a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe7a-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe7a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe7a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe7a-143">INPUTS</span></span>

## <span data-ttu-id="ffe7a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe7a-144">OUTPUTS</span></span>

## <span data-ttu-id="ffe7a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffe7a-145">NOTES</span></span>

## <span data-ttu-id="ffe7a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffe7a-146">RELATED LINKS</span></span>

[<span data-ttu-id="ffe7a-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="ffe7a-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


