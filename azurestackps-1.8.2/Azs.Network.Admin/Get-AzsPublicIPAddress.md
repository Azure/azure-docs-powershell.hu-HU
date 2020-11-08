---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016990"
---
# <span data-ttu-id="6588b-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="6588b-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="6588b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6588b-102">SYNOPSIS</span></span>
<span data-ttu-id="6588b-103">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="6588b-103">List of public IP addresses.</span></span>

## <span data-ttu-id="6588b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6588b-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6588b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6588b-105">DESCRIPTION</span></span>
<span data-ttu-id="6588b-106">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="6588b-106">List of public IP addresses.</span></span>

## <span data-ttu-id="6588b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6588b-107">EXAMPLES</span></span>

### <span data-ttu-id="6588b-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="6588b-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="6588b-109">A kiosztott vagy nem lefoglalt nyilvános IP-címek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6588b-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="6588b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6588b-110">PARAMETERS</span></span>

### <span data-ttu-id="6588b-111">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6588b-111">-Filter</span></span>
<span data-ttu-id="6588b-112">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="6588b-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6588b-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6588b-113">-OrderBy</span></span>
<span data-ttu-id="6588b-114">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="6588b-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6588b-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6588b-115">-Skip</span></span>
<span data-ttu-id="6588b-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6588b-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6588b-117">-Top</span><span class="sxs-lookup"><span data-stu-id="6588b-117">-Top</span></span>
<span data-ttu-id="6588b-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6588b-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6588b-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6588b-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6588b-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="6588b-120">-InlineCount</span></span>
<span data-ttu-id="6588b-121">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="6588b-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6588b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6588b-122">CommonParameters</span></span>
<span data-ttu-id="6588b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6588b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6588b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6588b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6588b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6588b-125">INPUTS</span></span>

## <span data-ttu-id="6588b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6588b-126">OUTPUTS</span></span>

### <span data-ttu-id="6588b-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6588b-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="6588b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6588b-128">NOTES</span></span>

## <span data-ttu-id="6588b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6588b-129">RELATED LINKS</span></span>
