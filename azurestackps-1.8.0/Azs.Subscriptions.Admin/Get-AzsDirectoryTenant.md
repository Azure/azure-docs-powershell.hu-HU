---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840357"
---
# <span data-ttu-id="14f14-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="14f14-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="14f14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14f14-102">SYNOPSIS</span></span>
<span data-ttu-id="14f14-103">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="14f14-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="14f14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14f14-104">SYNTAX</span></span>

### <span data-ttu-id="14f14-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14f14-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="14f14-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="14f14-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="14f14-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f14-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="14f14-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="14f14-108">DESCRIPTION</span></span>
<span data-ttu-id="14f14-109">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="14f14-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="14f14-110">Példák</span><span class="sxs-lookup"><span data-stu-id="14f14-110">EXAMPLES</span></span>

### <span data-ttu-id="14f14-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14f14-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="14f14-112">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="14f14-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="14f14-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14f14-113">PARAMETERS</span></span>

### <span data-ttu-id="14f14-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14f14-114">-Name</span></span>
<span data-ttu-id="14f14-115">Címtár-bérlő neve</span><span class="sxs-lookup"><span data-stu-id="14f14-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="14f14-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f14-116">-ResourceGroupName</span></span>
<span data-ttu-id="14f14-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="14f14-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="14f14-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f14-118">-ResourceId</span></span>
<span data-ttu-id="14f14-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="14f14-119">The resource id.</span></span>

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

### <span data-ttu-id="14f14-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="14f14-120">-Skip</span></span>
<span data-ttu-id="14f14-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="14f14-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="14f14-122">-Top</span><span class="sxs-lookup"><span data-stu-id="14f14-122">-Top</span></span>
<span data-ttu-id="14f14-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="14f14-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="14f14-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="14f14-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="14f14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f14-125">CommonParameters</span></span>
<span data-ttu-id="14f14-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14f14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f14-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f14-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f14-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f14-128">INPUTS</span></span>

## <span data-ttu-id="14f14-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14f14-129">OUTPUTS</span></span>

### <span data-ttu-id="14f14-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="14f14-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="14f14-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14f14-131">NOTES</span></span>

## <span data-ttu-id="14f14-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14f14-132">RELATED LINKS</span></span>

