---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015085"
---
# <span data-ttu-id="e42fb-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e42fb-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="e42fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e42fb-102">SYNOPSIS</span></span>


## <span data-ttu-id="e42fb-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e42fb-103">SYNTAX</span></span>

### <span data-ttu-id="e42fb-104">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e42fb-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e42fb-105">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e42fb-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e42fb-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e42fb-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e42fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e42fb-107">DESCRIPTION</span></span>


## <span data-ttu-id="e42fb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e42fb-108">EXAMPLES</span></span>

### <span data-ttu-id="e42fb-109">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="e42fb-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="e42fb-110">A tárterület-kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e42fb-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="e42fb-111">2. példa:</span><span class="sxs-lookup"><span data-stu-id="e42fb-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="e42fb-112">A megadott tárolási kvótáról a név alapján tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="e42fb-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="e42fb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e42fb-113">PARAMETERS</span></span>

### <span data-ttu-id="e42fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42fb-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="e42fb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e42fb-115">-InputObject</span></span>
<span data-ttu-id="e42fb-116">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e42fb-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e42fb-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="e42fb-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e42fb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e42fb-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e42fb-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e42fb-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e42fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42fb-120">CommonParameters</span></span>
<span data-ttu-id="e42fb-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e42fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42fb-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e42fb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42fb-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e42fb-123">INPUTS</span></span>

### <span data-ttu-id="e42fb-124">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e42fb-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="e42fb-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e42fb-125">OUTPUTS</span></span>

### <span data-ttu-id="e42fb-126">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e42fb-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="e42fb-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e42fb-127">NOTES</span></span>

<span data-ttu-id="e42fb-128">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e42fb-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e42fb-129">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e42fb-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e42fb-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e42fb-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="e42fb-131">`[AccountId <String>]`: Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="e42fb-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="e42fb-132">`[AsyncOperationId <String>]`: Aszinkron műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="e42fb-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="e42fb-133">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e42fb-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e42fb-134">`[Location <String>]`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e42fb-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="e42fb-135">`[QuotaName <String>]`: A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="e42fb-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="e42fb-136">`[ResourceGroup <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e42fb-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="e42fb-137">`[ServiceName <String>]`: Storage Service Name (tárterület neve)</span><span class="sxs-lookup"><span data-stu-id="e42fb-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="e42fb-138">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e42fb-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="e42fb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e42fb-139">RELATED LINKS</span></span>

