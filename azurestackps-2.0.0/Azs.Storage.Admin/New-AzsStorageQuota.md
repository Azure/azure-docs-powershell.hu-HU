---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844822"
---
# <span data-ttu-id="60664-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="60664-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="60664-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60664-102">SYNOPSIS</span></span>


## <span data-ttu-id="60664-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60664-103">SYNTAX</span></span>

### <span data-ttu-id="60664-104">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60664-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60664-105">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="60664-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60664-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="60664-106">DESCRIPTION</span></span>


## <span data-ttu-id="60664-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60664-107">EXAMPLES</span></span>

### <span data-ttu-id="60664-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="60664-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="60664-109">Új tárolási kvóta létrehozása megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="60664-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="60664-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60664-110">PARAMETERS</span></span>

### <span data-ttu-id="60664-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="60664-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="60664-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60664-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="60664-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="60664-113">-Location</span></span>


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

### <span data-ttu-id="60664-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60664-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="60664-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="60664-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="60664-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="60664-116">-QuotaObject</span></span>
<span data-ttu-id="60664-117">A kivitelezéshez tekintse meg a QUOTAOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="60664-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="60664-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60664-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="60664-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60664-119">-Confirm</span></span>
<span data-ttu-id="60664-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60664-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60664-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60664-121">-WhatIf</span></span>
<span data-ttu-id="60664-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60664-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60664-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60664-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60664-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60664-124">CommonParameters</span></span>
<span data-ttu-id="60664-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60664-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60664-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="60664-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60664-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60664-127">INPUTS</span></span>

### <span data-ttu-id="60664-128">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="60664-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="60664-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60664-129">OUTPUTS</span></span>

### <span data-ttu-id="60664-130">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="60664-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="60664-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60664-131">NOTES</span></span>

<span data-ttu-id="60664-132">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="60664-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60664-133">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="60664-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="60664-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="60664-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="60664-135">`[CapacityInGb <Int32?>]`: Maximális kapacitás (GB).</span><span class="sxs-lookup"><span data-stu-id="60664-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="60664-136">`[NumberOfStorageAccounts <Int32?>]`: A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="60664-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="60664-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60664-137">RELATED LINKS</span></span>

