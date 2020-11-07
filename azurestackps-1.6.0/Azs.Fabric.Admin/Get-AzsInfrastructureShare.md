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
ms.locfileid: "93671804"
---
# <span data-ttu-id="abb72-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="abb72-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="abb72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abb72-102">SYNOPSIS</span></span>
<span data-ttu-id="abb72-103">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="abb72-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="abb72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abb72-104">SYNTAX</span></span>

### <span data-ttu-id="abb72-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abb72-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb72-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="abb72-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb72-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb72-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="abb72-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abb72-108">DESCRIPTION</span></span>
<span data-ttu-id="abb72-109">A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="abb72-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="abb72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abb72-110">EXAMPLES</span></span>

### <span data-ttu-id="abb72-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="abb72-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="abb72-112">Az összes fájlmegosztás listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="abb72-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="abb72-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="abb72-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="abb72-114">A név alapján a fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="abb72-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="abb72-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abb72-115">PARAMETERS</span></span>

### <span data-ttu-id="abb72-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="abb72-116">-Filter</span></span>
<span data-ttu-id="abb72-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="abb72-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="abb72-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="abb72-118">-Location</span></span>
<span data-ttu-id="abb72-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="abb72-119">Location of the resource.</span></span>

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

### <span data-ttu-id="abb72-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abb72-120">-Name</span></span>
<span data-ttu-id="abb72-121">A szövet fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="abb72-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="abb72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb72-122">-ResourceGroupName</span></span>
<span data-ttu-id="abb72-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="abb72-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="abb72-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb72-124">-ResourceId</span></span>
<span data-ttu-id="abb72-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="abb72-125">The resource id.</span></span>

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

### <span data-ttu-id="abb72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb72-126">CommonParameters</span></span>
<span data-ttu-id="abb72-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abb72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb72-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb72-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb72-129">INPUTS</span></span>

## <span data-ttu-id="abb72-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb72-130">OUTPUTS</span></span>

### <span data-ttu-id="abb72-131">Microsoft. AzureStack. Management. Fabric. admin. models. fájlmegosztásról</span><span class="sxs-lookup"><span data-stu-id="abb72-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="abb72-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abb72-132">NOTES</span></span>

## <span data-ttu-id="abb72-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abb72-133">RELATED LINKS</span></span>

