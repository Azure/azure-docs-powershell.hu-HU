---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844818"
---
# <span data-ttu-id="bacb3-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="bacb3-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="bacb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bacb3-102">SYNOPSIS</span></span>


## <span data-ttu-id="bacb3-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bacb3-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bacb3-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="bacb3-104">DESCRIPTION</span></span>


## <span data-ttu-id="bacb3-105">Példák</span><span class="sxs-lookup"><span data-stu-id="bacb3-105">EXAMPLES</span></span>

### <span data-ttu-id="bacb3-106">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="bacb3-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="bacb3-107">Frissítse a tárolási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="bacb3-107">Update the storage settings.</span></span>

## <span data-ttu-id="bacb3-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bacb3-108">PARAMETERS</span></span>

### <span data-ttu-id="bacb3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacb3-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="bacb3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="bacb3-110">-Force</span></span>


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

### <span data-ttu-id="bacb3-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="bacb3-111">-Location</span></span>


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

### <span data-ttu-id="bacb3-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="bacb3-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


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

### <span data-ttu-id="bacb3-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bacb3-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="bacb3-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bacb3-114">-Confirm</span></span>
<span data-ttu-id="bacb3-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bacb3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bacb3-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bacb3-116">-WhatIf</span></span>
<span data-ttu-id="bacb3-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bacb3-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bacb3-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bacb3-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bacb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacb3-119">CommonParameters</span></span>
<span data-ttu-id="bacb3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bacb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacb3-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bacb3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacb3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bacb3-122">INPUTS</span></span>

## <span data-ttu-id="bacb3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bacb3-123">OUTPUTS</span></span>

### <span data-ttu-id="bacb3-124">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="bacb3-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="bacb3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bacb3-125">NOTES</span></span>

## <span data-ttu-id="bacb3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bacb3-126">RELATED LINKS</span></span>

