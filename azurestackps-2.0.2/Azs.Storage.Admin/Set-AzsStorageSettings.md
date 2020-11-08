---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017008"
---
# <span data-ttu-id="3f5cd-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="3f5cd-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="3f5cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f5cd-102">SYNOPSIS</span></span>


## <span data-ttu-id="3f5cd-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f5cd-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f5cd-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f5cd-104">DESCRIPTION</span></span>


## <span data-ttu-id="3f5cd-105">Példák</span><span class="sxs-lookup"><span data-stu-id="3f5cd-105">EXAMPLES</span></span>

### <span data-ttu-id="3f5cd-106">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="3f5cd-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="3f5cd-107">Frissítse a tárolási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-107">Update the storage settings.</span></span>

## <span data-ttu-id="3f5cd-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f5cd-108">PARAMETERS</span></span>

### <span data-ttu-id="3f5cd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5cd-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="3f5cd-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3f5cd-110">-Force</span></span>


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

### <span data-ttu-id="3f5cd-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="3f5cd-111">-Location</span></span>


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

### <span data-ttu-id="3f5cd-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="3f5cd-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f5cd-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f5cd-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="3f5cd-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f5cd-114">-Confirm</span></span>
<span data-ttu-id="3f5cd-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f5cd-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5cd-116">-WhatIf</span></span>
<span data-ttu-id="3f5cd-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f5cd-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f5cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5cd-119">CommonParameters</span></span>
<span data-ttu-id="3f5cd-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f5cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5cd-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5cd-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f5cd-122">INPUTS</span></span>

## <span data-ttu-id="3f5cd-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f5cd-123">OUTPUTS</span></span>

### <span data-ttu-id="3f5cd-124">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="3f5cd-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="3f5cd-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f5cd-125">NOTES</span></span>

## <span data-ttu-id="3f5cd-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f5cd-126">RELATED LINKS</span></span>

