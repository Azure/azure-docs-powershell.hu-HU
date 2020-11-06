---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491552"
---
# <span data-ttu-id="38578-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="38578-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="38578-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38578-102">SYNOPSIS</span></span>
<span data-ttu-id="38578-103">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="38578-103">Get the list of update locations.</span></span>

## <span data-ttu-id="38578-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38578-104">SYNTAX</span></span>

### <span data-ttu-id="38578-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38578-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="38578-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="38578-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="38578-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38578-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="38578-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38578-108">DESCRIPTION</span></span>
<span data-ttu-id="38578-109">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="38578-109">Get the list of update locations.</span></span> <span data-ttu-id="38578-110">A visszaadott helyek használhatók az elérhető frissítések eléréséhez a Get-AzsUpdate segítségével.</span><span class="sxs-lookup"><span data-stu-id="38578-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="38578-111">Példák</span><span class="sxs-lookup"><span data-stu-id="38578-111">EXAMPLES</span></span>

### <span data-ttu-id="38578-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="38578-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="38578-113">A frissítési helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="38578-113">Get the list of update locations.</span></span>

## <span data-ttu-id="38578-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38578-114">PARAMETERS</span></span>

### <span data-ttu-id="38578-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38578-115">-Name</span></span>
<span data-ttu-id="38578-116">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="38578-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38578-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38578-117">-ResourceGroupName</span></span>
<span data-ttu-id="38578-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="38578-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="38578-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38578-119">-ResourceId</span></span>
<span data-ttu-id="38578-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="38578-120">The resource id.</span></span>

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

### <span data-ttu-id="38578-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38578-121">CommonParameters</span></span>
<span data-ttu-id="38578-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38578-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38578-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38578-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38578-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38578-124">INPUTS</span></span>

## <span data-ttu-id="38578-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38578-125">OUTPUTS</span></span>

### <span data-ttu-id="38578-126">Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="38578-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="38578-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38578-127">NOTES</span></span>

## <span data-ttu-id="38578-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38578-128">RELATED LINKS</span></span>

