---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016961"
---
# <span data-ttu-id="485ce-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="485ce-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="485ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="485ce-102">SYNOPSIS</span></span>
<span data-ttu-id="485ce-103">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="485ce-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="485ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="485ce-104">SYNTAX</span></span>

### <span data-ttu-id="485ce-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="485ce-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="485ce-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="485ce-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="485ce-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="485ce-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="485ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="485ce-108">DESCRIPTION</span></span>
<span data-ttu-id="485ce-109">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="485ce-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="485ce-110">Példák</span><span class="sxs-lookup"><span data-stu-id="485ce-110">EXAMPLES</span></span>

### <span data-ttu-id="485ce-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="485ce-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="485ce-112">Az összes fájlmegosztás listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="485ce-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="485ce-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="485ce-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="485ce-114">A név alapján a fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="485ce-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="485ce-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="485ce-115">PARAMETERS</span></span>

### <span data-ttu-id="485ce-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="485ce-116">-Name</span></span>
<span data-ttu-id="485ce-117">A szövet fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="485ce-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="485ce-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="485ce-118">-Location</span></span>
<span data-ttu-id="485ce-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="485ce-119">Location of the resource.</span></span>

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

### <span data-ttu-id="485ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="485ce-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="485ce-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="485ce-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="485ce-122">-ResourceId</span></span>
<span data-ttu-id="485ce-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="485ce-123">The resource id.</span></span>

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

### <span data-ttu-id="485ce-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="485ce-124">-Filter</span></span>
<span data-ttu-id="485ce-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="485ce-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="485ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485ce-126">CommonParameters</span></span>
<span data-ttu-id="485ce-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="485ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485ce-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485ce-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="485ce-129">INPUTS</span></span>

## <span data-ttu-id="485ce-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="485ce-130">OUTPUTS</span></span>

### <span data-ttu-id="485ce-131">Microsoft. AzureStack. Management. Fabric. admin. models. fájlmegosztásról</span><span class="sxs-lookup"><span data-stu-id="485ce-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="485ce-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="485ce-132">NOTES</span></span>

## <span data-ttu-id="485ce-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="485ce-133">RELATED LINKS</span></span>
