---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840605"
---
# <span data-ttu-id="bbd8c-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bbd8c-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="bbd8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd8c-103">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbd8c-103">Get the list of update locations.</span></span>

## <span data-ttu-id="bbd8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbd8c-104">SYNTAX</span></span>

### <span data-ttu-id="bbd8c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbd8c-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bbd8c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbd8c-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bbd8c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd8c-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bbd8c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbd8c-108">DESCRIPTION</span></span>
<span data-ttu-id="bbd8c-109">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbd8c-109">Get the list of update locations.</span></span> <span data-ttu-id="bbd8c-110">A visszaadott helyek használhatók az elérhető frissítések eléréséhez a Get-AzsUpdate segítségével.</span><span class="sxs-lookup"><span data-stu-id="bbd8c-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="bbd8c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bbd8c-111">EXAMPLES</span></span>

### <span data-ttu-id="bbd8c-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="bbd8c-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="bbd8c-113">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbd8c-113">Get the list of update locations.</span></span>

## <span data-ttu-id="bbd8c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbd8c-114">PARAMETERS</span></span>

### <span data-ttu-id="bbd8c-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="bbd8c-115">-Location</span></span>
<span data-ttu-id="bbd8c-116">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="bbd8c-116">Name of the Location.</span></span>

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

### <span data-ttu-id="bbd8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bbd8c-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="bbd8c-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bbd8c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd8c-119">-ResourceId</span></span>
<span data-ttu-id="bbd8c-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bbd8c-120">The resource id.</span></span>

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

### <span data-ttu-id="bbd8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd8c-121">CommonParameters</span></span>
<span data-ttu-id="bbd8c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbd8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd8c-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd8c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd8c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd8c-124">INPUTS</span></span>

## <span data-ttu-id="bbd8c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd8c-125">OUTPUTS</span></span>

### <span data-ttu-id="bbd8c-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bbd8c-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="bbd8c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbd8c-127">NOTES</span></span>

## <span data-ttu-id="bbd8c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd8c-128">RELATED LINKS</span></span>
