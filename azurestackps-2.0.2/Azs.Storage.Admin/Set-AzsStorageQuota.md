---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016747"
---
# <span data-ttu-id="05145-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="05145-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="05145-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05145-102">SYNOPSIS</span></span>


## <span data-ttu-id="05145-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05145-103">SYNTAX</span></span>

### <span data-ttu-id="05145-104">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05145-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05145-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="05145-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="05145-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="05145-106">DESCRIPTION</span></span>


## <span data-ttu-id="05145-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05145-107">EXAMPLES</span></span>

### <span data-ttu-id="05145-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="05145-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="05145-109">Meglévő tárolási kvóta frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="05145-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="05145-110">2. példa:</span><span class="sxs-lookup"><span data-stu-id="05145-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="05145-111">A meglévő tárolási kvóták frissítése csővezetékek szerint.</span><span class="sxs-lookup"><span data-stu-id="05145-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="05145-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05145-112">PARAMETERS</span></span>

### <span data-ttu-id="05145-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="05145-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05145-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05145-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="05145-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="05145-115">-Location</span></span>


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

### <span data-ttu-id="05145-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05145-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05145-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="05145-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05145-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="05145-118">-QuotaObject</span></span>
<span data-ttu-id="05145-119">A kivitelezéshez tekintse meg a QUOTAOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05145-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="05145-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05145-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="05145-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05145-121">-Confirm</span></span>
<span data-ttu-id="05145-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05145-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05145-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05145-123">-WhatIf</span></span>
<span data-ttu-id="05145-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05145-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05145-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05145-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05145-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05145-126">CommonParameters</span></span>
<span data-ttu-id="05145-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05145-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05145-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05145-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05145-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05145-129">INPUTS</span></span>

### <span data-ttu-id="05145-130">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="05145-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="05145-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05145-131">OUTPUTS</span></span>

### <span data-ttu-id="05145-132">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="05145-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="05145-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05145-133">NOTES</span></span>

<span data-ttu-id="05145-134">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05145-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05145-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="05145-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05145-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="05145-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="05145-137">`[CapacityInGb <Int32?>]`: Maximális kapacitás (GB).</span><span class="sxs-lookup"><span data-stu-id="05145-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="05145-138">`[NumberOfStorageAccounts <Int32?>]`: A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="05145-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="05145-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05145-139">RELATED LINKS</span></span>

