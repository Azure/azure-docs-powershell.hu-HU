---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840548"
---
# <span data-ttu-id="986c8-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="986c8-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="986c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="986c8-102">SYNOPSIS</span></span>
<span data-ttu-id="986c8-103">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="986c8-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="986c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="986c8-104">SYNTAX</span></span>

### <span data-ttu-id="986c8-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="986c8-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="986c8-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="986c8-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="986c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="986c8-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="986c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="986c8-108">DESCRIPTION</span></span>
<span data-ttu-id="986c8-109">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="986c8-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="986c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="986c8-110">EXAMPLES</span></span>

### <span data-ttu-id="986c8-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="986c8-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="986c8-112">Az összes fájlmegosztás listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="986c8-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="986c8-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="986c8-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="986c8-114">A név alapján a fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="986c8-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="986c8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="986c8-115">PARAMETERS</span></span>

### <span data-ttu-id="986c8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="986c8-116">-Name</span></span>
<span data-ttu-id="986c8-117">A szövet fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="986c8-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="986c8-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="986c8-118">-Location</span></span>
<span data-ttu-id="986c8-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="986c8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="986c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="986c8-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="986c8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="986c8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="986c8-122">-ResourceId</span></span>
<span data-ttu-id="986c8-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="986c8-123">The resource id.</span></span>

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

### <span data-ttu-id="986c8-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="986c8-124">-Filter</span></span>
<span data-ttu-id="986c8-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="986c8-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986c8-126">CommonParameters</span></span>
<span data-ttu-id="986c8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="986c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986c8-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986c8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986c8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="986c8-129">INPUTS</span></span>

## <span data-ttu-id="986c8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="986c8-130">OUTPUTS</span></span>

### <span data-ttu-id="986c8-131">Microsoft. AzureStack. Management. Fabric. admin. models. fájlmegosztásról</span><span class="sxs-lookup"><span data-stu-id="986c8-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="986c8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="986c8-132">NOTES</span></span>

## <span data-ttu-id="986c8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="986c8-133">RELATED LINKS</span></span>
