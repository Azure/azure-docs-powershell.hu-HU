---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491347"
---
# <span data-ttu-id="9cfc6-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cfc6-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="9cfc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cfc6-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfc6-103">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="9cfc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cfc6-104">SYNTAX</span></span>

### <span data-ttu-id="9cfc6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cfc6-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9cfc6-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="9cfc6-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9cfc6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cfc6-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="9cfc6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cfc6-108">DESCRIPTION</span></span>
<span data-ttu-id="9cfc6-109">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="9cfc6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9cfc6-110">EXAMPLES</span></span>

### <span data-ttu-id="9cfc6-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9cfc6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="9cfc6-112">A tárolási fiókok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9cfc6-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="9cfc6-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9cfc6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="9cfc6-114">Információkat kaphat a megadott tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="9cfc6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cfc6-115">PARAMETERS</span></span>

### <span data-ttu-id="9cfc6-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9cfc6-116">-FarmName</span></span>
<span data-ttu-id="9cfc6-117">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-117">Farm Id.</span></span>

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

### <span data-ttu-id="9cfc6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cfc6-118">-Name</span></span>
<span data-ttu-id="9cfc6-119">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="9cfc6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfc6-120">-ResourceGroupName</span></span>
<span data-ttu-id="9cfc6-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-121">Resource group name.</span></span>

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

### <span data-ttu-id="9cfc6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cfc6-122">-ResourceId</span></span>
<span data-ttu-id="9cfc6-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-123">The resource id.</span></span>

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

### <span data-ttu-id="9cfc6-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="9cfc6-124">-Skip</span></span>
<span data-ttu-id="9cfc6-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9cfc6-126">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="9cfc6-126">-Summary</span></span>
<span data-ttu-id="9cfc6-127">Váltson a köszörülés összegzésére vagy a részletes információkra.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-127">Switch for wheter summary or detailed information is returned.</span></span>

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

### <span data-ttu-id="9cfc6-128">-Top</span><span class="sxs-lookup"><span data-stu-id="9cfc6-128">-Top</span></span>
<span data-ttu-id="9cfc6-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9cfc6-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="9cfc6-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9cfc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfc6-131">CommonParameters</span></span>
<span data-ttu-id="9cfc6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cfc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfc6-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfc6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfc6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cfc6-134">INPUTS</span></span>

## <span data-ttu-id="9cfc6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cfc6-135">OUTPUTS</span></span>

### <span data-ttu-id="9cfc6-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cfc6-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="9cfc6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cfc6-137">NOTES</span></span>

## <span data-ttu-id="9cfc6-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cfc6-138">RELATED LINKS</span></span>

