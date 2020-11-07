---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840415"
---
# <span data-ttu-id="19051-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="19051-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="19051-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19051-102">SYNOPSIS</span></span>
<span data-ttu-id="19051-103">A blob-acquistions listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="19051-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="19051-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19051-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="19051-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19051-105">DESCRIPTION</span></span>
<span data-ttu-id="19051-106">A blob-acquistions listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="19051-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="19051-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19051-107">EXAMPLES</span></span>

### <span data-ttu-id="19051-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="19051-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="19051-109">A blob-acquistions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="19051-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="19051-110">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="19051-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="19051-111">A blob-acquistions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="19051-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="19051-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19051-112">PARAMETERS</span></span>

### <span data-ttu-id="19051-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="19051-113">-FarmName</span></span>
<span data-ttu-id="19051-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="19051-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19051-115">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="19051-115">-Filter</span></span>
<span data-ttu-id="19051-116">Karakterlánc szűrése</span><span class="sxs-lookup"><span data-stu-id="19051-116">Filter string</span></span>

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

### <span data-ttu-id="19051-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19051-117">-ResourceGroupName</span></span>
<span data-ttu-id="19051-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="19051-118">Resource group name.</span></span>

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

### <span data-ttu-id="19051-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19051-119">CommonParameters</span></span>
<span data-ttu-id="19051-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19051-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19051-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19051-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19051-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19051-122">INPUTS</span></span>

## <span data-ttu-id="19051-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19051-123">OUTPUTS</span></span>

## <span data-ttu-id="19051-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19051-124">NOTES</span></span>

## <span data-ttu-id="19051-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19051-125">RELATED LINKS</span></span>

