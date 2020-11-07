---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840657"
---
# <span data-ttu-id="6fe97-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="6fe97-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="6fe97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fe97-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe97-103">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6fe97-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6fe97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fe97-104">SYNTAX</span></span>

### <span data-ttu-id="6fe97-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fe97-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6fe97-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6fe97-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6fe97-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe97-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6fe97-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fe97-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe97-109">A tároló gazdaságok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6fe97-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6fe97-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6fe97-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe97-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="6fe97-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="6fe97-112">A tárolási gazdaságok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6fe97-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="6fe97-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fe97-113">PARAMETERS</span></span>

### <span data-ttu-id="6fe97-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fe97-114">-Name</span></span>
<span data-ttu-id="6fe97-115">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="6fe97-115">Farm Id.</span></span>

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

### <span data-ttu-id="6fe97-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe97-116">-ResourceGroupName</span></span>
<span data-ttu-id="6fe97-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6fe97-117">Resource group name.</span></span>

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

### <span data-ttu-id="6fe97-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe97-118">-ResourceId</span></span>
<span data-ttu-id="6fe97-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6fe97-119">The resource id.</span></span>

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

### <span data-ttu-id="6fe97-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6fe97-120">-Skip</span></span>
<span data-ttu-id="6fe97-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6fe97-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6fe97-122">-Top</span><span class="sxs-lookup"><span data-stu-id="6fe97-122">-Top</span></span>
<span data-ttu-id="6fe97-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6fe97-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6fe97-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6fe97-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6fe97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe97-125">CommonParameters</span></span>
<span data-ttu-id="6fe97-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fe97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe97-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe97-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe97-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe97-128">INPUTS</span></span>

## <span data-ttu-id="6fe97-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe97-129">OUTPUTS</span></span>

### <span data-ttu-id="6fe97-130">Microsoft. AzureStack. Management. Storage. admin. models. Farm</span><span class="sxs-lookup"><span data-stu-id="6fe97-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="6fe97-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fe97-131">NOTES</span></span>

## <span data-ttu-id="6fe97-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe97-132">RELATED LINKS</span></span>
