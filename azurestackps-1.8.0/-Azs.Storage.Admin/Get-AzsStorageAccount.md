---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840416"
---
# <span data-ttu-id="d9fa5-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9fa5-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="d9fa5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fa5-103">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="d9fa5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9fa5-104">SYNTAX</span></span>

### <span data-ttu-id="d9fa5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9fa5-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d9fa5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d9fa5-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9fa5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fa5-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="d9fa5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9fa5-108">DESCRIPTION</span></span>
<span data-ttu-id="d9fa5-109">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="d9fa5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d9fa5-110">EXAMPLES</span></span>

### <span data-ttu-id="d9fa5-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9fa5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="d9fa5-112">A tárolási fiókok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d9fa5-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="d9fa5-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9fa5-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="d9fa5-114">Információkat kaphat a megadott tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="d9fa5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9fa5-115">PARAMETERS</span></span>

### <span data-ttu-id="d9fa5-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d9fa5-116">-FarmName</span></span>
<span data-ttu-id="d9fa5-117">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-117">Farm Id.</span></span>

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

### <span data-ttu-id="d9fa5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9fa5-118">-Name</span></span>
<span data-ttu-id="d9fa5-119">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="d9fa5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fa5-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9fa5-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-121">Resource group name.</span></span>

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

### <span data-ttu-id="d9fa5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fa5-122">-ResourceId</span></span>
<span data-ttu-id="d9fa5-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-123">The resource id.</span></span>

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

### <span data-ttu-id="d9fa5-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="d9fa5-124">-Skip</span></span>
<span data-ttu-id="d9fa5-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d9fa5-126">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="d9fa5-126">-Summary</span></span>
<span data-ttu-id="d9fa5-127">Váltson a köszörülés összegzésére vagy a részletes információkra.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-127">Switch for wheter summary or detailed information is returned.</span></span>

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

### <span data-ttu-id="d9fa5-128">-Top</span><span class="sxs-lookup"><span data-stu-id="d9fa5-128">-Top</span></span>
<span data-ttu-id="d9fa5-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d9fa5-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="d9fa5-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d9fa5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fa5-131">CommonParameters</span></span>
<span data-ttu-id="d9fa5-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9fa5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fa5-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fa5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fa5-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9fa5-134">INPUTS</span></span>

## <span data-ttu-id="d9fa5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9fa5-135">OUTPUTS</span></span>

### <span data-ttu-id="d9fa5-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9fa5-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="d9fa5-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9fa5-137">NOTES</span></span>

## <span data-ttu-id="d9fa5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9fa5-138">RELATED LINKS</span></span>

