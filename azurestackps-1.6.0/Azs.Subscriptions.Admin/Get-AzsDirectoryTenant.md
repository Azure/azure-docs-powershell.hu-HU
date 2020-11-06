---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490800"
---
# <span data-ttu-id="e9585-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="e9585-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="e9585-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9585-102">SYNOPSIS</span></span>
<span data-ttu-id="e9585-103">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e9585-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e9585-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9585-104">SYNTAX</span></span>

### <span data-ttu-id="e9585-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9585-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e9585-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e9585-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9585-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9585-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9585-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9585-108">DESCRIPTION</span></span>
<span data-ttu-id="e9585-109">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e9585-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e9585-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e9585-110">EXAMPLES</span></span>

### <span data-ttu-id="e9585-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9585-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="e9585-112">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e9585-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="e9585-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9585-113">PARAMETERS</span></span>

### <span data-ttu-id="e9585-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9585-114">-Name</span></span>
<span data-ttu-id="e9585-115">Címtár-bérlő neve</span><span class="sxs-lookup"><span data-stu-id="e9585-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="e9585-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9585-116">-ResourceGroupName</span></span>
<span data-ttu-id="e9585-117">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e9585-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e9585-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9585-118">-ResourceId</span></span>
<span data-ttu-id="e9585-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e9585-119">The resource id.</span></span>

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

### <span data-ttu-id="e9585-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e9585-120">-Skip</span></span>
<span data-ttu-id="e9585-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e9585-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e9585-122">-Top</span><span class="sxs-lookup"><span data-stu-id="e9585-122">-Top</span></span>
<span data-ttu-id="e9585-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e9585-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9585-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e9585-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e9585-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9585-125">CommonParameters</span></span>
<span data-ttu-id="e9585-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9585-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9585-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9585-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9585-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9585-128">INPUTS</span></span>

## <span data-ttu-id="e9585-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9585-129">OUTPUTS</span></span>

### <span data-ttu-id="e9585-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="e9585-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="e9585-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9585-131">NOTES</span></span>

## <span data-ttu-id="e9585-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9585-132">RELATED LINKS</span></span>

