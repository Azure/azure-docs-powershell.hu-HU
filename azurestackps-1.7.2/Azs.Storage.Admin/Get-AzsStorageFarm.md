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
ms.locfileid: "93839488"
---
# <span data-ttu-id="a8c2f-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="a8c2f-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="a8c2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c2f-103">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="a8c2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8c2f-104">SYNTAX</span></span>

### <span data-ttu-id="a8c2f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8c2f-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a8c2f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a8c2f-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8c2f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c2f-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a8c2f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8c2f-108">DESCRIPTION</span></span>
<span data-ttu-id="a8c2f-109">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="a8c2f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8c2f-110">EXAMPLES</span></span>

### <span data-ttu-id="a8c2f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8c2f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="a8c2f-112">A tárolási gazdaságok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a8c2f-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="a8c2f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8c2f-113">PARAMETERS</span></span>

### <span data-ttu-id="a8c2f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8c2f-114">-Name</span></span>
<span data-ttu-id="a8c2f-115">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-115">Farm Id.</span></span>

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

### <span data-ttu-id="a8c2f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c2f-116">-ResourceGroupName</span></span>
<span data-ttu-id="a8c2f-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-117">Resource group name.</span></span>

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

### <span data-ttu-id="a8c2f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c2f-118">-ResourceId</span></span>
<span data-ttu-id="a8c2f-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-119">The resource id.</span></span>

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

### <span data-ttu-id="a8c2f-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a8c2f-120">-Skip</span></span>
<span data-ttu-id="a8c2f-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a8c2f-122">-Top</span><span class="sxs-lookup"><span data-stu-id="a8c2f-122">-Top</span></span>
<span data-ttu-id="a8c2f-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a8c2f-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a8c2f-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a8c2f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c2f-125">CommonParameters</span></span>
<span data-ttu-id="a8c2f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8c2f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c2f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c2f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c2f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c2f-128">INPUTS</span></span>

## <span data-ttu-id="a8c2f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c2f-129">OUTPUTS</span></span>

### <span data-ttu-id="a8c2f-130">Microsoft. AzureStack. Management. Storage. admin. models. Farm</span><span class="sxs-lookup"><span data-stu-id="a8c2f-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="a8c2f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8c2f-131">NOTES</span></span>

## <span data-ttu-id="a8c2f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8c2f-132">RELATED LINKS</span></span>

