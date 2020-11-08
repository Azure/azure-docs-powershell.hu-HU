---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015155"
---
# <span data-ttu-id="a5e4f-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="a5e4f-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="a5e4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5e4f-102">SYNOPSIS</span></span>


## <span data-ttu-id="a5e4f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5e4f-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5e4f-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5e4f-104">DESCRIPTION</span></span>


## <span data-ttu-id="a5e4f-105">Példák</span><span class="sxs-lookup"><span data-stu-id="a5e4f-105">EXAMPLES</span></span>

### <span data-ttu-id="a5e4f-106">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="a5e4f-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="a5e4f-107">Indítsa el a Garbage gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-107">Start garbage collection.</span></span>

## <span data-ttu-id="a5e4f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5e4f-108">PARAMETERS</span></span>

### <span data-ttu-id="a5e4f-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5e4f-109">-AsJob</span></span>


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

### <span data-ttu-id="a5e4f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e4f-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="a5e4f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a5e4f-111">-Force</span></span>


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

### <span data-ttu-id="a5e4f-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5e4f-112">-Location</span></span>


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

### <span data-ttu-id="a5e4f-113">-Várva</span><span class="sxs-lookup"><span data-stu-id="a5e4f-113">-NoWait</span></span>


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

### <span data-ttu-id="a5e4f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5e4f-114">-PassThru</span></span>


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

### <span data-ttu-id="a5e4f-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5e4f-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="a5e4f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5e4f-116">-Confirm</span></span>
<span data-ttu-id="a5e4f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e4f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e4f-118">-WhatIf</span></span>
<span data-ttu-id="a5e4f-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e4f-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e4f-121">CommonParameters</span></span>
<span data-ttu-id="a5e4f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5e4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e4f-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e4f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e4f-124">INPUTS</span></span>

## <span data-ttu-id="a5e4f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e4f-125">OUTPUTS</span></span>

### <span data-ttu-id="a5e4f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e4f-126">System.Boolean</span></span>



## <span data-ttu-id="a5e4f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5e4f-127">NOTES</span></span>

## <span data-ttu-id="a5e4f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5e4f-128">RELATED LINKS</span></span>

