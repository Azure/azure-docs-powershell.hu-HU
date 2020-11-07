---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840437"
---
# <span data-ttu-id="b19d0-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="b19d0-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="b19d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b19d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b19d0-103">A várólista szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b19d0-103">Returns the queue service.</span></span>

## <span data-ttu-id="b19d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b19d0-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="b19d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b19d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b19d0-106">A várólista szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b19d0-106">Returns the queue service.</span></span>

## <span data-ttu-id="b19d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b19d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b19d0-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b19d0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b19d0-109">A várólista-szolgáltatás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="b19d0-109">Get the queue service.</span></span>

## <span data-ttu-id="b19d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b19d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b19d0-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b19d0-111">-FarmName</span></span>
<span data-ttu-id="b19d0-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="b19d0-112">Farm Id.</span></span>

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

### <span data-ttu-id="b19d0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b19d0-113">-ResourceGroupName</span></span>
<span data-ttu-id="b19d0-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b19d0-114">Resource group name.</span></span>

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

### <span data-ttu-id="b19d0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19d0-115">CommonParameters</span></span>
<span data-ttu-id="b19d0-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b19d0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19d0-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b19d0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19d0-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b19d0-118">INPUTS</span></span>

## <span data-ttu-id="b19d0-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b19d0-119">OUTPUTS</span></span>

### <span data-ttu-id="b19d0-120">Microsoft. AzureStack. Management. Storage. admin. models. QueueService</span><span class="sxs-lookup"><span data-stu-id="b19d0-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="b19d0-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b19d0-121">NOTES</span></span>

## <span data-ttu-id="b19d0-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b19d0-122">RELATED LINKS</span></span>

