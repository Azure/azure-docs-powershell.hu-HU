---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3996096b692a7e242fc6cf42288508bdc4625cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491667"
---
# <span data-ttu-id="b1819-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b1819-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="b1819-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1819-102">SYNOPSIS</span></span>
<span data-ttu-id="b1819-103">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="b1819-103">List of public IP addresses.</span></span>

## <span data-ttu-id="b1819-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1819-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1819-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1819-105">DESCRIPTION</span></span>
<span data-ttu-id="b1819-106">Nyilvános IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="b1819-106">List of public IP addresses.</span></span>

## <span data-ttu-id="b1819-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1819-107">EXAMPLES</span></span>

### <span data-ttu-id="b1819-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1819-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="b1819-109">A kiosztott vagy nem lefoglalt nyilvános IP-címek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1819-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="b1819-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1819-110">PARAMETERS</span></span>

### <span data-ttu-id="b1819-111">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b1819-111">-Filter</span></span>
<span data-ttu-id="b1819-112">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b1819-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="b1819-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b1819-113">-InlineCount</span></span>
<span data-ttu-id="b1819-114">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="b1819-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b1819-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b1819-115">-OrderBy</span></span>
<span data-ttu-id="b1819-116">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="b1819-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b1819-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b1819-117">-Skip</span></span>
<span data-ttu-id="b1819-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b1819-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b1819-119">-Top</span><span class="sxs-lookup"><span data-stu-id="b1819-119">-Top</span></span>
<span data-ttu-id="b1819-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b1819-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b1819-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b1819-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b1819-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1819-122">CommonParameters</span></span>
<span data-ttu-id="b1819-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1819-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1819-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1819-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1819-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1819-125">INPUTS</span></span>

## <span data-ttu-id="b1819-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1819-126">OUTPUTS</span></span>

### <span data-ttu-id="b1819-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1819-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="b1819-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1819-128">NOTES</span></span>

## <span data-ttu-id="b1819-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1819-129">RELATED LINKS</span></span>

