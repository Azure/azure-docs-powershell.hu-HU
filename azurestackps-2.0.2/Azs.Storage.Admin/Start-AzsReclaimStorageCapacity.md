---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016606"
---
# <span data-ttu-id="5fe19-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="5fe19-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="5fe19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fe19-102">SYNOPSIS</span></span>


## <span data-ttu-id="5fe19-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fe19-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fe19-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fe19-104">DESCRIPTION</span></span>


## <span data-ttu-id="5fe19-105">Példák</span><span class="sxs-lookup"><span data-stu-id="5fe19-105">EXAMPLES</span></span>

### <span data-ttu-id="5fe19-106">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="5fe19-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="5fe19-107">Indítsa el a Garbage gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5fe19-107">Start garbage collection.</span></span>

## <span data-ttu-id="5fe19-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fe19-108">PARAMETERS</span></span>

### <span data-ttu-id="5fe19-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fe19-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe19-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5fe19-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="5fe19-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-113">-Várva</span><span class="sxs-lookup"><span data-stu-id="5fe19-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fe19-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fe19-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fe19-116">-Confirm</span></span>
<span data-ttu-id="5fe19-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fe19-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe19-118">-WhatIf</span></span>
<span data-ttu-id="5fe19-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fe19-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe19-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fe19-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5fe19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe19-121">CommonParameters</span></span>
<span data-ttu-id="5fe19-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fe19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe19-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fe19-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe19-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe19-124">INPUTS</span></span>

## <span data-ttu-id="5fe19-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe19-125">OUTPUTS</span></span>

### <span data-ttu-id="5fe19-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fe19-126">System.Boolean</span></span>



## <span data-ttu-id="5fe19-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fe19-127">NOTES</span></span>

## <span data-ttu-id="5fe19-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fe19-128">RELATED LINKS</span></span>

