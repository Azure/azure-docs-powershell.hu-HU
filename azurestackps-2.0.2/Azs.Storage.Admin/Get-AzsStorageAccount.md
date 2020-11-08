---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016654"
---
# <span data-ttu-id="ffc4b-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffc4b-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="ffc4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc4b-103">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="ffc4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffc4b-104">SYNTAX</span></span>

### <span data-ttu-id="ffc4b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ffc4b-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ffc4b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="ffc4b-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ffc4b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ffc4b-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ffc4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffc4b-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc4b-109">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="ffc4b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ffc4b-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc4b-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="ffc4b-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="ffc4b-112">A raktározási fiókok listáját (összefoglalás) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="ffc4b-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="ffc4b-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="ffc4b-114">Megtudhatja, hogy milyen tárterületet tartalmazó tárterülete van, és hogyan nyomtathatja ki az állapotot.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="ffc4b-115">3. példa:</span><span class="sxs-lookup"><span data-stu-id="ffc4b-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="ffc4b-116">Információkat kaphat a megadott tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="ffc4b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffc4b-117">PARAMETERS</span></span>

### <span data-ttu-id="ffc4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc4b-118">-DefaultProfile</span></span>
<span data-ttu-id="ffc4b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc4b-120">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="ffc4b-120">-Filter</span></span>
<span data-ttu-id="ffc4b-121">Karakterlánc szűrése</span><span class="sxs-lookup"><span data-stu-id="ffc4b-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffc4b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc4b-122">-InputObject</span></span>
<span data-ttu-id="ffc4b-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ffc4b-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="ffc4b-124">-Location</span></span>
<span data-ttu-id="ffc4b-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-125">Resource location.</span></span>

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

### <span data-ttu-id="ffc4b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffc4b-126">-Name</span></span>
<span data-ttu-id="ffc4b-127">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffc4b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffc4b-128">-SubscriptionId</span></span>
<span data-ttu-id="ffc4b-129">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="ffc4b-129">Subscription Id.</span></span>

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

### <span data-ttu-id="ffc4b-130">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="ffc4b-130">-Summary</span></span>
<span data-ttu-id="ffc4b-131">Annak megadása, hogy az Összegzés vagy a részletes információk visszaadása</span><span class="sxs-lookup"><span data-stu-id="ffc4b-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ffc4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc4b-132">CommonParameters</span></span>
<span data-ttu-id="ffc4b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffc4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc4b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc4b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffc4b-135">INPUTS</span></span>

### <span data-ttu-id="ffc4b-136">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ffc4b-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="ffc4b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffc4b-137">OUTPUTS</span></span>

### <span data-ttu-id="ffc4b-138">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffc4b-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="ffc4b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffc4b-139">NOTES</span></span>

<span data-ttu-id="ffc4b-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ffc4b-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ffc4b-142">INPUTOBJECT <IStorageAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ffc4b-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ffc4b-143">`[AccountId <String>]`: Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="ffc4b-144">`[AsyncOperationId <String>]`: Aszinkron műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="ffc4b-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ffc4b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ffc4b-146">`[Location <String>]`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="ffc4b-147">`[QuotaName <String>]`: A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="ffc4b-148">`[ResourceGroup <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ffc4b-149">`[ServiceName <String>]`: Storage Service Name (tárterület neve)</span><span class="sxs-lookup"><span data-stu-id="ffc4b-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="ffc4b-150">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ffc4b-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="ffc4b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffc4b-151">RELATED LINKS</span></span>

