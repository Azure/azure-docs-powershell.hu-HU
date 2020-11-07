---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840602"
---
# <span data-ttu-id="d5a92-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="d5a92-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="d5a92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5a92-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a92-103">A tárterület-megosztások listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d5a92-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="d5a92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5a92-104">SYNTAX</span></span>

### <span data-ttu-id="d5a92-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5a92-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d5a92-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5a92-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d5a92-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a92-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d5a92-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5a92-108">DESCRIPTION</span></span>
<span data-ttu-id="d5a92-109">A tárterület-megosztások listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d5a92-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="d5a92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d5a92-110">EXAMPLES</span></span>

### <span data-ttu-id="d5a92-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="d5a92-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d5a92-112">A tárterület-megosztások listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5a92-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="d5a92-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5a92-113">PARAMETERS</span></span>

### <span data-ttu-id="d5a92-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d5a92-114">-FarmName</span></span>
<span data-ttu-id="d5a92-115">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="d5a92-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a92-116">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="d5a92-116">-ShareName</span></span>
<span data-ttu-id="d5a92-117">Megosztási név.</span><span class="sxs-lookup"><span data-stu-id="d5a92-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a92-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a92-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5a92-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d5a92-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a92-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a92-120">-ResourceId</span></span>
<span data-ttu-id="d5a92-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d5a92-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a92-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a92-122">CommonParameters</span></span>
<span data-ttu-id="d5a92-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5a92-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a92-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a92-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a92-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a92-125">INPUTS</span></span>

## <span data-ttu-id="d5a92-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a92-126">OUTPUTS</span></span>

### <span data-ttu-id="d5a92-127">Microsoft. AzureStack. Management. Storage. admin. models. share</span><span class="sxs-lookup"><span data-stu-id="d5a92-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="d5a92-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5a92-128">NOTES</span></span>

## <span data-ttu-id="d5a92-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5a92-129">RELATED LINKS</span></span>
