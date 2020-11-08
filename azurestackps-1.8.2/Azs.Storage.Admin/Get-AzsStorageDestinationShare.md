---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016888"
---
# <span data-ttu-id="c6ebc-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="c6ebc-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="c6ebc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ebc-103">A címzettek listájának értékét számítja ki az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="c6ebc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6ebc-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6ebc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="c6ebc-106">A címzettek listájának értékét számítja ki az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="c6ebc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="c6ebc-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="c6ebc-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="c6ebc-109">Itt megtekintheti a célhelyek listáját, amelyeket a rendszer a legjobbnak ítéli meg az áttelepítés megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="c6ebc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6ebc-110">PARAMETERS</span></span>

### <span data-ttu-id="c6ebc-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="c6ebc-111">-SourceShareName</span></span>
<span data-ttu-id="c6ebc-112">Annak a megosztásnak a neve, amelybe áttelepíteni kívánja a tárolókat.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="c6ebc-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="c6ebc-113">-FarmName</span></span>
<span data-ttu-id="c6ebc-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-114">Farm Id.</span></span>

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

### <span data-ttu-id="c6ebc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ebc-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6ebc-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c6ebc-116">Resource group name.</span></span>

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

### <span data-ttu-id="c6ebc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ebc-117">CommonParameters</span></span>
<span data-ttu-id="c6ebc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6ebc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ebc-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ebc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ebc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6ebc-120">INPUTS</span></span>

## <span data-ttu-id="c6ebc-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6ebc-121">OUTPUTS</span></span>

## <span data-ttu-id="c6ebc-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6ebc-122">NOTES</span></span>

## <span data-ttu-id="c6ebc-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6ebc-123">RELATED LINKS</span></span>
