---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015204"
---
# <span data-ttu-id="40553-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="40553-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="40553-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40553-102">SYNOPSIS</span></span>
<span data-ttu-id="40553-103">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="40553-103">List of public ip addresses.</span></span>

## <span data-ttu-id="40553-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40553-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="40553-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40553-105">DESCRIPTION</span></span>
<span data-ttu-id="40553-106">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="40553-106">List of public ip addresses.</span></span>

## <span data-ttu-id="40553-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40553-107">EXAMPLES</span></span>

### <span data-ttu-id="40553-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40553-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="40553-109">A kiosztott vagy nem lefoglalt nyilvános IP-címek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="40553-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="40553-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40553-110">PARAMETERS</span></span>

### <span data-ttu-id="40553-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40553-111">-DefaultProfile</span></span>
<span data-ttu-id="40553-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40553-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="40553-113">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="40553-113">-Filter</span></span>
<span data-ttu-id="40553-114">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="40553-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="40553-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="40553-115">-InlineCount</span></span>
<span data-ttu-id="40553-116">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="40553-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="40553-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="40553-117">-OrderBy</span></span>
<span data-ttu-id="40553-118">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="40553-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="40553-119">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="40553-119">-Skip</span></span>
<span data-ttu-id="40553-120">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="40553-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="40553-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40553-121">-SubscriptionId</span></span>
<span data-ttu-id="40553-122">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="40553-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="40553-123">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="40553-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="40553-124">-Top</span><span class="sxs-lookup"><span data-stu-id="40553-124">-Top</span></span>
<span data-ttu-id="40553-125">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="40553-125">OData top parameter.</span></span>

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

### <span data-ttu-id="40553-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40553-126">CommonParameters</span></span>
<span data-ttu-id="40553-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40553-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40553-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40553-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40553-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40553-129">INPUTS</span></span>

## <span data-ttu-id="40553-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40553-130">OUTPUTS</span></span>

### <span data-ttu-id="40553-131">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="40553-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="40553-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40553-132">NOTES</span></span>

## <span data-ttu-id="40553-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40553-133">RELATED LINKS</span></span>

