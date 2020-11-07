---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840104"
---
# <span data-ttu-id="1a5aa-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="1a5aa-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="1a5aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5aa-103">A rendelkezésre álló frissítések listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-103">Get the list of available updates.</span></span>

## <span data-ttu-id="1a5aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a5aa-104">SYNTAX</span></span>

### <span data-ttu-id="1a5aa-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a5aa-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a5aa-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1a5aa-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a5aa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a5aa-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1a5aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a5aa-108">DESCRIPTION</span></span>
<span data-ttu-id="1a5aa-109">A rendelkezésre álló frissítések listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-109">Get the list of available updates.</span></span> <span data-ttu-id="1a5aa-110">Előfordulhat, hogy a modulból visszaadott frissítések a "telepítési-AzsUpdate", ha lehetséges.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="1a5aa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1a5aa-111">EXAMPLES</span></span>

### <span data-ttu-id="1a5aa-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a5aa-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="1a5aa-113">A rendelkezésre álló frissítések listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-113">Get the list of available updates.</span></span>

### <span data-ttu-id="1a5aa-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a5aa-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="1a5aa-115">A megadott frissítés beszerzése</span><span class="sxs-lookup"><span data-stu-id="1a5aa-115">Get the specific update.</span></span>

## <span data-ttu-id="1a5aa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a5aa-116">PARAMETERS</span></span>

### <span data-ttu-id="1a5aa-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1a5aa-117">-Location</span></span>
<span data-ttu-id="1a5aa-118">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-118">The name of the update location.</span></span>

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

### <span data-ttu-id="1a5aa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a5aa-119">-Name</span></span>
<span data-ttu-id="1a5aa-120">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-120">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a5aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a5aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a5aa-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1a5aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a5aa-123">-ResourceId</span></span>
<span data-ttu-id="1a5aa-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-124">The resource id.</span></span>

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

### <span data-ttu-id="1a5aa-125">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="1a5aa-125">-Skip</span></span>
<span data-ttu-id="1a5aa-126">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1a5aa-127">-Top</span><span class="sxs-lookup"><span data-stu-id="1a5aa-127">-Top</span></span>
<span data-ttu-id="1a5aa-128">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1a5aa-129">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="1a5aa-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1a5aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5aa-130">CommonParameters</span></span>
<span data-ttu-id="1a5aa-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a5aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5aa-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5aa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5aa-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a5aa-133">INPUTS</span></span>

## <span data-ttu-id="1a5aa-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a5aa-134">OUTPUTS</span></span>

### <span data-ttu-id="1a5aa-135">Microsoft. AzureStack. Management. Update. admin. modellek. Update</span><span class="sxs-lookup"><span data-stu-id="1a5aa-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="1a5aa-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a5aa-136">NOTES</span></span>

## <span data-ttu-id="1a5aa-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a5aa-137">RELATED LINKS</span></span>

