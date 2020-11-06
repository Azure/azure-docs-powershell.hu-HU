---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490883"
---
# <span data-ttu-id="b5f5a-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="b5f5a-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="b5f5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f5a-103">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="b5f5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5f5a-104">SYNTAX</span></span>

### <span data-ttu-id="b5f5a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5f5a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5f5a-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5f5a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f5a-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b5f5a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5f5a-108">DESCRIPTION</span></span>
<span data-ttu-id="b5f5a-109">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="b5f5a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5f5a-110">EXAMPLES</span></span>

### <span data-ttu-id="b5f5a-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5f5a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="b5f5a-112">Az összes fájlmegosztás listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="b5f5a-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5f5a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="b5f5a-114">A név alapján a fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="b5f5a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5f5a-115">PARAMETERS</span></span>

### <span data-ttu-id="b5f5a-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b5f5a-116">-Filter</span></span>
<span data-ttu-id="b5f5a-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b5f5a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b5f5a-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="b5f5a-118">-Location</span></span>
<span data-ttu-id="b5f5a-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b5f5a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-120">-Name</span></span>
<span data-ttu-id="b5f5a-121">A szövet fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="b5f5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5f5a-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b5f5a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f5a-124">-ResourceId</span></span>
<span data-ttu-id="b5f5a-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-125">The resource id.</span></span>

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

### <span data-ttu-id="b5f5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f5a-126">CommonParameters</span></span>
<span data-ttu-id="b5f5a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5f5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f5a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f5a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f5a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5f5a-129">INPUTS</span></span>

## <span data-ttu-id="b5f5a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5f5a-130">OUTPUTS</span></span>

### <span data-ttu-id="b5f5a-131">Microsoft. AzureStack. Management. Fabric. admin. models. fájlmegosztásról</span><span class="sxs-lookup"><span data-stu-id="b5f5a-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="b5f5a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5f5a-132">NOTES</span></span>

## <span data-ttu-id="b5f5a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5f5a-133">RELATED LINKS</span></span>

