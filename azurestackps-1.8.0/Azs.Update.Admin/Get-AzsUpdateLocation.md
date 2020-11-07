---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840304"
---
# <span data-ttu-id="0097d-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="0097d-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="0097d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0097d-102">SYNOPSIS</span></span>
<span data-ttu-id="0097d-103">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0097d-103">Get the list of update locations.</span></span>

## <span data-ttu-id="0097d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0097d-104">SYNTAX</span></span>

### <span data-ttu-id="0097d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0097d-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0097d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0097d-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0097d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0097d-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0097d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0097d-108">DESCRIPTION</span></span>
<span data-ttu-id="0097d-109">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0097d-109">Get the list of update locations.</span></span> <span data-ttu-id="0097d-110">A visszaadott helyek használhatók az elérhető frissítések eléréséhez a Get-AzsUpdate segítségével.</span><span class="sxs-lookup"><span data-stu-id="0097d-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="0097d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0097d-111">EXAMPLES</span></span>

### <span data-ttu-id="0097d-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="0097d-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="0097d-113">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0097d-113">Get the list of update locations.</span></span>

## <span data-ttu-id="0097d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0097d-114">PARAMETERS</span></span>

### <span data-ttu-id="0097d-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="0097d-115">-Location</span></span>
<span data-ttu-id="0097d-116">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="0097d-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0097d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0097d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0097d-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="0097d-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0097d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0097d-119">-ResourceId</span></span>
<span data-ttu-id="0097d-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0097d-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0097d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0097d-121">CommonParameters</span></span>
<span data-ttu-id="0097d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0097d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0097d-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0097d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0097d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0097d-124">INPUTS</span></span>

## <span data-ttu-id="0097d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0097d-125">OUTPUTS</span></span>

### <span data-ttu-id="0097d-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="0097d-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="0097d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0097d-127">NOTES</span></span>

## <span data-ttu-id="0097d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0097d-128">RELATED LINKS</span></span>
