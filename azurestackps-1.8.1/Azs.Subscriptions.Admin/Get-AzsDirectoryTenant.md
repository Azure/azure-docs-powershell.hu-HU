---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840516"
---
# <span data-ttu-id="11450-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="11450-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="11450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11450-102">SYNOPSIS</span></span>
<span data-ttu-id="11450-103">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="11450-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="11450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11450-104">SYNTAX</span></span>

### <span data-ttu-id="11450-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11450-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="11450-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="11450-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="11450-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11450-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="11450-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11450-108">DESCRIPTION</span></span>
<span data-ttu-id="11450-109">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="11450-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="11450-110">Példák</span><span class="sxs-lookup"><span data-stu-id="11450-110">EXAMPLES</span></span>

### <span data-ttu-id="11450-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11450-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="11450-112">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="11450-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="11450-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11450-113">PARAMETERS</span></span>

### <span data-ttu-id="11450-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11450-114">-Name</span></span>
<span data-ttu-id="11450-115">Címtár-bérlő neve</span><span class="sxs-lookup"><span data-stu-id="11450-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="11450-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11450-116">-ResourceGroupName</span></span>
<span data-ttu-id="11450-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="11450-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="11450-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11450-118">-ResourceId</span></span>
<span data-ttu-id="11450-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="11450-119">The resource id.</span></span>

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

### <span data-ttu-id="11450-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="11450-120">-Skip</span></span>
<span data-ttu-id="11450-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="11450-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="11450-122">-Top</span><span class="sxs-lookup"><span data-stu-id="11450-122">-Top</span></span>
<span data-ttu-id="11450-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="11450-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="11450-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="11450-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="11450-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11450-125">CommonParameters</span></span>
<span data-ttu-id="11450-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11450-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11450-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11450-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11450-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11450-128">INPUTS</span></span>

## <span data-ttu-id="11450-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11450-129">OUTPUTS</span></span>

### <span data-ttu-id="11450-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="11450-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="11450-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11450-131">NOTES</span></span>

## <span data-ttu-id="11450-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11450-132">RELATED LINKS</span></span>

