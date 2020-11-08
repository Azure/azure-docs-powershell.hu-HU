---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181479"
---
# <span data-ttu-id="25324-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="25324-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="25324-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25324-102">SYNOPSIS</span></span>
<span data-ttu-id="25324-103">A Microsoft által kínált társközi helyek bevonása</span><span class="sxs-lookup"><span data-stu-id="25324-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="25324-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25324-104">SYNTAX</span></span>

### <span data-ttu-id="25324-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25324-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25324-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="25324-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25324-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="25324-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25324-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="25324-108">DESCRIPTION</span></span>
<span data-ttu-id="25324-109">Itt érheti el azokat a társközi lehetőségeket, amelyekben a felhasználók kapcsolatba léphetnek a KARJÁN.</span><span class="sxs-lookup"><span data-stu-id="25324-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="25324-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25324-110">EXAMPLES</span></span>

### <span data-ttu-id="25324-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25324-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="25324-112">A helyek hosszú listája.</span><span class="sxs-lookup"><span data-stu-id="25324-112">Its a long list of locations.</span></span> <span data-ttu-id="25324-113">Az összes közvetlen társas létesítményt kapja.</span><span class="sxs-lookup"><span data-stu-id="25324-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="25324-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="25324-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="25324-115">Megkapja a Honolulu-beli Exchange-alapú levelezés helyét.</span><span class="sxs-lookup"><span data-stu-id="25324-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="25324-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="25324-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="25324-117">Megkeresi az Exchange-alapú levelezés helyét a 71-ös peer-azonosítóban.</span><span class="sxs-lookup"><span data-stu-id="25324-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="25324-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25324-118">PARAMETERS</span></span>

### <span data-ttu-id="25324-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25324-119">-DefaultProfile</span></span>
<span data-ttu-id="25324-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25324-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25324-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="25324-121">-DirectPeeringType</span></span>
<span data-ttu-id="25324-122">Válassza az "Edge", a "CDN" és a "tranzit" parancsot.</span><span class="sxs-lookup"><span data-stu-id="25324-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25324-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="25324-123">-Kind</span></span>
<span data-ttu-id="25324-124">A teljes egyenrangú erőforrást jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="25324-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25324-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="25324-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="25324-126">A PeeringDB.com-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="25324-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25324-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="25324-127">-PeeringLocation</span></span>
<span data-ttu-id="25324-128">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="25324-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25324-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25324-129">CommonParameters</span></span>
<span data-ttu-id="25324-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25324-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25324-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25324-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25324-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25324-132">INPUTS</span></span>

### <span data-ttu-id="25324-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="25324-133">None</span></span>

## <span data-ttu-id="25324-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25324-134">OUTPUTS</span></span>

### <span data-ttu-id="25324-135">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="25324-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="25324-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25324-136">NOTES</span></span>

## <span data-ttu-id="25324-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25324-137">RELATED LINKS</span></span>
