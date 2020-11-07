---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838699"
---
# <span data-ttu-id="d264e-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d264e-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="d264e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d264e-102">SYNOPSIS</span></span>
<span data-ttu-id="d264e-103">Az összes virtuális hálózat listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d264e-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="d264e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d264e-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d264e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d264e-105">DESCRIPTION</span></span>
<span data-ttu-id="d264e-106">Az összes virtuális hálózat listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d264e-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="d264e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d264e-107">EXAMPLES</span></span>

### <span data-ttu-id="d264e-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d264e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="d264e-109">Az Azure halom bélyegző virtuális hálózatainak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d264e-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="d264e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d264e-110">PARAMETERS</span></span>

### <span data-ttu-id="d264e-111">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="d264e-111">-Filter</span></span>
<span data-ttu-id="d264e-112">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="d264e-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="d264e-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="d264e-113">-InlineCount</span></span>
<span data-ttu-id="d264e-114">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="d264e-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="d264e-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d264e-115">-OrderBy</span></span>
<span data-ttu-id="d264e-116">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="d264e-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="d264e-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="d264e-117">-Skip</span></span>
<span data-ttu-id="d264e-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="d264e-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d264e-119">-Top</span><span class="sxs-lookup"><span data-stu-id="d264e-119">-Top</span></span>
<span data-ttu-id="d264e-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="d264e-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d264e-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="d264e-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d264e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d264e-122">CommonParameters</span></span>
<span data-ttu-id="d264e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d264e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d264e-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d264e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d264e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d264e-125">INPUTS</span></span>

## <span data-ttu-id="d264e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d264e-126">OUTPUTS</span></span>

### <span data-ttu-id="d264e-127">Microsoft. AzureStack. Management. Network. admin. models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d264e-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="d264e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d264e-128">NOTES</span></span>

## <span data-ttu-id="d264e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d264e-129">RELATED LINKS</span></span>

