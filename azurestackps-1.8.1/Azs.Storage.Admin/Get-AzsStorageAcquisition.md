---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840666"
---
# <span data-ttu-id="53929-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="53929-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="53929-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53929-102">SYNOPSIS</span></span>
<span data-ttu-id="53929-103">A blob-acquistions listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="53929-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="53929-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53929-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="53929-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53929-105">DESCRIPTION</span></span>
<span data-ttu-id="53929-106">A blob-acquistions listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="53929-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="53929-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53929-107">EXAMPLES</span></span>

### <span data-ttu-id="53929-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="53929-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="53929-109">A blob-acquistions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="53929-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="53929-110">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="53929-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="53929-111">A blob-acquistions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="53929-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="53929-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53929-112">PARAMETERS</span></span>

### <span data-ttu-id="53929-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="53929-113">-FarmName</span></span>
<span data-ttu-id="53929-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="53929-114">Farm Id.</span></span>

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

### <span data-ttu-id="53929-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53929-115">-ResourceGroupName</span></span>
<span data-ttu-id="53929-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="53929-116">Resource group name.</span></span>

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

### <span data-ttu-id="53929-117">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="53929-117">-Filter</span></span>
<span data-ttu-id="53929-118">Karakterlánc szűrése</span><span class="sxs-lookup"><span data-stu-id="53929-118">Filter string</span></span>

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

### <span data-ttu-id="53929-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53929-119">CommonParameters</span></span>
<span data-ttu-id="53929-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53929-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53929-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53929-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53929-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53929-122">INPUTS</span></span>

## <span data-ttu-id="53929-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53929-123">OUTPUTS</span></span>

## <span data-ttu-id="53929-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53929-124">NOTES</span></span>

## <span data-ttu-id="53929-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53929-125">RELATED LINKS</span></span>
