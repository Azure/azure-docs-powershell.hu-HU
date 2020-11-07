---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671764"
---
# <span data-ttu-id="be3b0-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="be3b0-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="be3b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="be3b0-103">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="be3b0-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="be3b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be3b0-104">SYNTAX</span></span>

### <span data-ttu-id="be3b0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be3b0-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="be3b0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="be3b0-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="be3b0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="be3b0-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="be3b0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="be3b0-108">DESCRIPTION</span></span>
<span data-ttu-id="be3b0-109">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="be3b0-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="be3b0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="be3b0-110">EXAMPLES</span></span>

### <span data-ttu-id="be3b0-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="be3b0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="be3b0-112">A tárolási gazdaságok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="be3b0-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="be3b0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be3b0-113">PARAMETERS</span></span>

### <span data-ttu-id="be3b0-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be3b0-114">-Name</span></span>
<span data-ttu-id="be3b0-115">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="be3b0-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3b0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3b0-116">-ResourceGroupName</span></span>
<span data-ttu-id="be3b0-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="be3b0-117">Resource group name.</span></span>

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

### <span data-ttu-id="be3b0-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be3b0-118">-ResourceId</span></span>
<span data-ttu-id="be3b0-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="be3b0-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3b0-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="be3b0-120">-Skip</span></span>
<span data-ttu-id="be3b0-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="be3b0-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3b0-122">-Top</span><span class="sxs-lookup"><span data-stu-id="be3b0-122">-Top</span></span>
<span data-ttu-id="be3b0-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="be3b0-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="be3b0-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="be3b0-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3b0-125">CommonParameters</span></span>
<span data-ttu-id="be3b0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be3b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3b0-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3b0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be3b0-128">INPUTS</span></span>

## <span data-ttu-id="be3b0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be3b0-129">OUTPUTS</span></span>

### <span data-ttu-id="be3b0-130">Microsoft. AzureStack. Management. Storage. admin. models. Farm</span><span class="sxs-lookup"><span data-stu-id="be3b0-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="be3b0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be3b0-131">NOTES</span></span>

## <span data-ttu-id="be3b0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be3b0-132">RELATED LINKS</span></span>

