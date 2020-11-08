---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016750"
---
# <span data-ttu-id="9aa42-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="9aa42-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="9aa42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9aa42-102">SYNOPSIS</span></span>


## <span data-ttu-id="9aa42-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9aa42-103">SYNTAX</span></span>

### <span data-ttu-id="9aa42-104">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9aa42-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9aa42-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9aa42-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9aa42-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="9aa42-106">DESCRIPTION</span></span>


## <span data-ttu-id="9aa42-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9aa42-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa42-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="9aa42-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="9aa42-109">Tárolási kvóta eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="9aa42-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="9aa42-110">2. példa:</span><span class="sxs-lookup"><span data-stu-id="9aa42-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="9aa42-111">Tárolási kvóta eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9aa42-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="9aa42-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9aa42-112">PARAMETERS</span></span>

### <span data-ttu-id="9aa42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa42-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="9aa42-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aa42-114">-InputObject</span></span>
<span data-ttu-id="9aa42-115">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9aa42-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9aa42-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="9aa42-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9aa42-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9aa42-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9aa42-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aa42-118">-PassThru</span></span>


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

### <span data-ttu-id="9aa42-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9aa42-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9aa42-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9aa42-120">-Confirm</span></span>
<span data-ttu-id="9aa42-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9aa42-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aa42-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa42-122">-WhatIf</span></span>
<span data-ttu-id="9aa42-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9aa42-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aa42-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9aa42-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aa42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa42-125">CommonParameters</span></span>
<span data-ttu-id="9aa42-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9aa42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa42-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9aa42-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa42-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa42-128">INPUTS</span></span>

### <span data-ttu-id="9aa42-129">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9aa42-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="9aa42-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa42-130">OUTPUTS</span></span>

### <span data-ttu-id="9aa42-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9aa42-131">System.Boolean</span></span>



## <span data-ttu-id="9aa42-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9aa42-132">NOTES</span></span>

<span data-ttu-id="9aa42-133">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9aa42-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9aa42-134">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9aa42-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9aa42-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="9aa42-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="9aa42-136">`[AccountId <String>]`: Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="9aa42-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="9aa42-137">`[AsyncOperationId <String>]`: Aszinkron műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="9aa42-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="9aa42-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9aa42-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9aa42-139">`[Location <String>]`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="9aa42-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="9aa42-140">`[QuotaName <String>]`: A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="9aa42-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="9aa42-141">`[ResourceGroup <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9aa42-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="9aa42-142">`[ServiceName <String>]`: Storage Service Name (tárterület neve)</span><span class="sxs-lookup"><span data-stu-id="9aa42-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="9aa42-143">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9aa42-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="9aa42-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9aa42-144">RELATED LINKS</span></span>

