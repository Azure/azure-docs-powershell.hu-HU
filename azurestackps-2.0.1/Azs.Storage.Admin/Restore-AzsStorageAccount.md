---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/25/2020
ms.locfileid: "94015387"
---
# <span data-ttu-id="bafde-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafde-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="bafde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bafde-102">SYNOPSIS</span></span>


## <span data-ttu-id="bafde-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bafde-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bafde-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="bafde-104">DESCRIPTION</span></span>


## <span data-ttu-id="bafde-105">Példák</span><span class="sxs-lookup"><span data-stu-id="bafde-105">EXAMPLES</span></span>

### <span data-ttu-id="bafde-106">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="bafde-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="bafde-107">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="bafde-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="bafde-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bafde-108">PARAMETERS</span></span>

### <span data-ttu-id="bafde-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bafde-109">-AsJob</span></span>


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

### <span data-ttu-id="bafde-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafde-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="bafde-111">-Force</span><span class="sxs-lookup"><span data-stu-id="bafde-111">-Force</span></span>


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

### <span data-ttu-id="bafde-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="bafde-112">-Location</span></span>


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

### <span data-ttu-id="bafde-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bafde-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bafde-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="bafde-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bafde-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="bafde-115">-NoWait</span></span>


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

### <span data-ttu-id="bafde-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bafde-116">-PassThru</span></span>


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

### <span data-ttu-id="bafde-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bafde-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="bafde-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bafde-118">-Confirm</span></span>
<span data-ttu-id="bafde-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bafde-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafde-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafde-120">-WhatIf</span></span>
<span data-ttu-id="bafde-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bafde-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafde-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bafde-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafde-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafde-123">CommonParameters</span></span>
<span data-ttu-id="bafde-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bafde-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafde-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bafde-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafde-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bafde-126">INPUTS</span></span>

## <span data-ttu-id="bafde-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bafde-127">OUTPUTS</span></span>

### <span data-ttu-id="bafde-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bafde-128">System.Boolean</span></span>



## <span data-ttu-id="bafde-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bafde-129">NOTES</span></span>

## <span data-ttu-id="bafde-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bafde-130">RELATED LINKS</span></span>

