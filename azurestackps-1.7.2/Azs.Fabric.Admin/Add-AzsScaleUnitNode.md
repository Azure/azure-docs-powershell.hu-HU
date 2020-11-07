---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840119"
---
# <span data-ttu-id="813f2-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="813f2-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="813f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="813f2-102">SYNOPSIS</span></span>
<span data-ttu-id="813f2-103">Méretarány kiosztása</span><span class="sxs-lookup"><span data-stu-id="813f2-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="813f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="813f2-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="813f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="813f2-105">DESCRIPTION</span></span>
<span data-ttu-id="813f2-106">Adjon hozzá egy új méretarányos csomópontot a méretarányos fürthöz.</span><span class="sxs-lookup"><span data-stu-id="813f2-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="813f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="813f2-107">EXAMPLES</span></span>

### <span data-ttu-id="813f2-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="813f2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="813f2-109">A csomópontok listáját hozzáadja a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="813f2-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="813f2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="813f2-110">PARAMETERS</span></span>

### <span data-ttu-id="813f2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="813f2-111">-AsJob</span></span>
<span data-ttu-id="813f2-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="813f2-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="813f2-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="813f2-114">Várjon, amíg a tárterület-replikáció a sikeres visszatérés előtt befejeződött.</span><span class="sxs-lookup"><span data-stu-id="813f2-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="813f2-115">-Location</span></span>
<span data-ttu-id="813f2-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="813f2-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="813f2-117">-NodeList</span></span>
<span data-ttu-id="813f2-118">A méretarány-csomópontok készletének hozzáadását lehetővé tevő bemeneti adatok listája.</span><span class="sxs-lookup"><span data-stu-id="813f2-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="813f2-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="813f2-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="813f2-121">-ScaleUnit</span></span>
<span data-ttu-id="813f2-122">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="813f2-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813f2-123">CommonParameters</span></span>
<span data-ttu-id="813f2-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="813f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813f2-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813f2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813f2-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="813f2-126">INPUTS</span></span>

## <span data-ttu-id="813f2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="813f2-127">OUTPUTS</span></span>

## <span data-ttu-id="813f2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="813f2-128">NOTES</span></span>

## <span data-ttu-id="813f2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="813f2-129">RELATED LINKS</span></span>

