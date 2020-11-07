---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4ec0639e31df3766550d6f7acc655cd3b5608bf
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840682"
---
# <span data-ttu-id="e3d4b-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3d4b-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="e3d4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d4b-103">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="e3d4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3d4b-104">SYNTAX</span></span>

### <span data-ttu-id="e3d4b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3d4b-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e3d4b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3d4b-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3d4b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d4b-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3d4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="e3d4b-109">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="e3d4b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e3d4b-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d4b-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="e3d4b-111">EXAMPLE 1</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="e3d4b-112">A tárolási fiókok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3d4b-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="e3d4b-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="e3d4b-113">EXAMPLE 2</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="e3d4b-114">Információkat kaphat a megadott tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="e3d4b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3d4b-115">PARAMETERS</span></span>

### <span data-ttu-id="e3d4b-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="e3d4b-116">-FarmName</span></span>
<span data-ttu-id="e3d4b-117">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-117">Farm Id.</span></span>

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

### <span data-ttu-id="e3d4b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3d4b-118">-Name</span></span>
<span data-ttu-id="e3d4b-119">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3d4b-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-121">Resource group name.</span></span>

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

### <span data-ttu-id="e3d4b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d4b-122">-ResourceId</span></span>
<span data-ttu-id="e3d4b-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d4b-124">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="e3d4b-124">-Summary</span></span>
<span data-ttu-id="e3d4b-125">Váltson a köszörülés összegzésére vagy a részletes információkra.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-125">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d4b-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e3d4b-126">-Skip</span></span>
<span data-ttu-id="e3d4b-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e3d4b-128">-Top</span><span class="sxs-lookup"><span data-stu-id="e3d4b-128">-Top</span></span>
<span data-ttu-id="e3d4b-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e3d4b-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e3d4b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e3d4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d4b-131">CommonParameters</span></span>
<span data-ttu-id="e3d4b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3d4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d4b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d4b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d4b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3d4b-134">INPUTS</span></span>

## <span data-ttu-id="e3d4b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3d4b-135">OUTPUTS</span></span>

### <span data-ttu-id="e3d4b-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3d4b-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="e3d4b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3d4b-137">NOTES</span></span>

## <span data-ttu-id="e3d4b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3d4b-138">RELATED LINKS</span></span>
