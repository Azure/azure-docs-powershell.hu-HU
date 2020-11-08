---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016898"
---
# <span data-ttu-id="d5a9f-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="d5a9f-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="d5a9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a9f-103">A várólista szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d5a9f-103">Returns the queue service.</span></span>

## <span data-ttu-id="d5a9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5a9f-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="d5a9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a9f-106">A várólista szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d5a9f-106">Returns the queue service.</span></span>

## <span data-ttu-id="d5a9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5a9f-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a9f-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="d5a9f-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d5a9f-109">A várólista-szolgáltatás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d5a9f-109">Get the queue service.</span></span>

## <span data-ttu-id="d5a9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5a9f-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a9f-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d5a9f-111">-FarmName</span></span>
<span data-ttu-id="d5a9f-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="d5a9f-112">Farm Id.</span></span>

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

### <span data-ttu-id="d5a9f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a9f-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5a9f-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d5a9f-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a9f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a9f-115">CommonParameters</span></span>
<span data-ttu-id="d5a9f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5a9f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a9f-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a9f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a9f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a9f-118">INPUTS</span></span>

## <span data-ttu-id="d5a9f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a9f-119">OUTPUTS</span></span>

### <span data-ttu-id="d5a9f-120">Microsoft. AzureStack. Management. Storage. admin. models. QueueService</span><span class="sxs-lookup"><span data-stu-id="d5a9f-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="d5a9f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5a9f-121">NOTES</span></span>

## <span data-ttu-id="d5a9f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5a9f-122">RELATED LINKS</span></span>
