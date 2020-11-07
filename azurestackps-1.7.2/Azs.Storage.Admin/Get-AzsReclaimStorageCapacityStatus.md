---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838682"
---
# <span data-ttu-id="b1b74-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="b1b74-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="b1b74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1b74-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b74-103">A Garbage Collection Job állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1b74-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="b1b74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1b74-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1b74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1b74-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b74-106">A Garbage Collection Job állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1b74-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="b1b74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1b74-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b74-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1b74-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="b1b74-109">Információt ad vissza a Garbage-gyűjtemény állapotáról.</span><span class="sxs-lookup"><span data-stu-id="b1b74-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="b1b74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1b74-110">PARAMETERS</span></span>

### <span data-ttu-id="b1b74-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b1b74-111">-FarmName</span></span>
<span data-ttu-id="b1b74-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="b1b74-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b74-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="b1b74-113">-JobId</span></span>
<span data-ttu-id="b1b74-114">Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="b1b74-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b74-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b74-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1b74-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b1b74-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b74-117">CommonParameters</span></span>
<span data-ttu-id="b1b74-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1b74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b74-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b74-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b74-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b74-120">INPUTS</span></span>

## <span data-ttu-id="b1b74-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b74-121">OUTPUTS</span></span>

## <span data-ttu-id="b1b74-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1b74-122">NOTES</span></span>

## <span data-ttu-id="b1b74-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1b74-123">RELATED LINKS</span></span>

