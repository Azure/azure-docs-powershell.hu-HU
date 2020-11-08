---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016964"
---
# <span data-ttu-id="94fd7-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94fd7-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="94fd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="94fd7-103">Az összes virtuális hálózat listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="94fd7-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="94fd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94fd7-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94fd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="94fd7-106">Az összes virtuális hálózat listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="94fd7-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="94fd7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="94fd7-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="94fd7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="94fd7-109">Az Azure halom bélyegző virtuális hálózatainak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="94fd7-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="94fd7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94fd7-110">PARAMETERS</span></span>

### <span data-ttu-id="94fd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fd7-111">-DefaultProfile</span></span>
<span data-ttu-id="94fd7-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94fd7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94fd7-113">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="94fd7-113">-Filter</span></span>
<span data-ttu-id="94fd7-114">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="94fd7-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="94fd7-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="94fd7-115">-InlineCount</span></span>
<span data-ttu-id="94fd7-116">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="94fd7-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="94fd7-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="94fd7-117">-OrderBy</span></span>
<span data-ttu-id="94fd7-118">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="94fd7-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="94fd7-119">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="94fd7-119">-Skip</span></span>
<span data-ttu-id="94fd7-120">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="94fd7-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="94fd7-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94fd7-121">-SubscriptionId</span></span>
<span data-ttu-id="94fd7-122">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="94fd7-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94fd7-123">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94fd7-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94fd7-124">-Top</span><span class="sxs-lookup"><span data-stu-id="94fd7-124">-Top</span></span>
<span data-ttu-id="94fd7-125">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="94fd7-125">OData top parameter.</span></span>

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

### <span data-ttu-id="94fd7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fd7-126">CommonParameters</span></span>
<span data-ttu-id="94fd7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94fd7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fd7-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94fd7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fd7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fd7-129">INPUTS</span></span>

## <span data-ttu-id="94fd7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fd7-130">OUTPUTS</span></span>

### <span data-ttu-id="94fd7-131">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94fd7-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="94fd7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94fd7-132">NOTES</span></span>

## <span data-ttu-id="94fd7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94fd7-133">RELATED LINKS</span></span>

