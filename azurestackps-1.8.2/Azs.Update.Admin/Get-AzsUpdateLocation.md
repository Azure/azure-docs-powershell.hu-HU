---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016935"
---
# <span data-ttu-id="05905-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="05905-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="05905-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05905-102">SYNOPSIS</span></span>
<span data-ttu-id="05905-103">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="05905-103">Get the list of update locations.</span></span>

## <span data-ttu-id="05905-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05905-104">SYNTAX</span></span>

### <span data-ttu-id="05905-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05905-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="05905-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="05905-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="05905-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="05905-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="05905-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05905-108">DESCRIPTION</span></span>
<span data-ttu-id="05905-109">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="05905-109">Get the list of update locations.</span></span> <span data-ttu-id="05905-110">A visszaadott helyek használhatók az elérhető frissítések eléréséhez a Get-AzsUpdate segítségével.</span><span class="sxs-lookup"><span data-stu-id="05905-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="05905-111">Példák</span><span class="sxs-lookup"><span data-stu-id="05905-111">EXAMPLES</span></span>

### <span data-ttu-id="05905-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="05905-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="05905-113">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="05905-113">Get the list of update locations.</span></span>

## <span data-ttu-id="05905-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05905-114">PARAMETERS</span></span>

### <span data-ttu-id="05905-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="05905-115">-Location</span></span>
<span data-ttu-id="05905-116">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="05905-116">Name of the Location.</span></span>

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

### <span data-ttu-id="05905-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05905-117">-ResourceGroupName</span></span>
<span data-ttu-id="05905-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="05905-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="05905-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05905-119">-ResourceId</span></span>
<span data-ttu-id="05905-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="05905-120">The resource id.</span></span>

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

### <span data-ttu-id="05905-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05905-121">CommonParameters</span></span>
<span data-ttu-id="05905-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05905-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05905-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05905-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05905-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05905-124">INPUTS</span></span>

## <span data-ttu-id="05905-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05905-125">OUTPUTS</span></span>

### <span data-ttu-id="05905-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="05905-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="05905-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05905-127">NOTES</span></span>

## <span data-ttu-id="05905-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05905-128">RELATED LINKS</span></span>
