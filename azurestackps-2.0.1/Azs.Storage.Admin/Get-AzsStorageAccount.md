---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015327"
---
# <span data-ttu-id="0e433-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e433-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="0e433-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e433-102">SYNOPSIS</span></span>
<span data-ttu-id="0e433-103">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0e433-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="0e433-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e433-104">SYNTAX</span></span>

### <span data-ttu-id="0e433-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e433-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e433-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e433-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e433-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e433-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0e433-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e433-108">DESCRIPTION</span></span>
<span data-ttu-id="0e433-109">A kért tárterület-fiókot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0e433-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="0e433-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0e433-110">EXAMPLES</span></span>

### <span data-ttu-id="0e433-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="0e433-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="0e433-112">A raktározási fiókok listáját (összefoglalás) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e433-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="0e433-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="0e433-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="0e433-114">Megtudhatja, hogy milyen tárterületet tartalmazó tárterülete van, és hogyan nyomtathatja ki az állapotot.</span><span class="sxs-lookup"><span data-stu-id="0e433-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="0e433-115">3. példa:</span><span class="sxs-lookup"><span data-stu-id="0e433-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="0e433-116">Információkat kaphat a megadott tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="0e433-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="0e433-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e433-117">PARAMETERS</span></span>

### <span data-ttu-id="0e433-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e433-118">-DefaultProfile</span></span>
<span data-ttu-id="0e433-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e433-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e433-120">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="0e433-120">-Filter</span></span>
<span data-ttu-id="0e433-121">Karakterlánc szűrése</span><span class="sxs-lookup"><span data-stu-id="0e433-121">Filter string</span></span>

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

### <span data-ttu-id="0e433-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e433-122">-InputObject</span></span>
<span data-ttu-id="0e433-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e433-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e433-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="0e433-124">-Location</span></span>
<span data-ttu-id="0e433-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0e433-125">Resource location.</span></span>

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

### <span data-ttu-id="0e433-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e433-126">-Name</span></span>
<span data-ttu-id="0e433-127">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="0e433-127">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="0e433-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e433-128">-SubscriptionId</span></span>
<span data-ttu-id="0e433-129">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="0e433-129">Subscription Id.</span></span>

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

### <span data-ttu-id="0e433-130">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="0e433-130">-Summary</span></span>
<span data-ttu-id="0e433-131">Annak megadása, hogy az Összegzés vagy a részletes információk visszaadása</span><span class="sxs-lookup"><span data-stu-id="0e433-131">Switch for whether summary or detailed information is returned.</span></span>

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

### <span data-ttu-id="0e433-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e433-132">CommonParameters</span></span>
<span data-ttu-id="0e433-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e433-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e433-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e433-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e433-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e433-135">INPUTS</span></span>

### <span data-ttu-id="0e433-136">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0e433-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="0e433-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e433-137">OUTPUTS</span></span>

### <span data-ttu-id="0e433-138">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e433-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="0e433-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e433-139">NOTES</span></span>

<span data-ttu-id="0e433-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0e433-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e433-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0e433-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0e433-142">INPUTOBJECT <IStorageAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0e433-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e433-143">`[AccountId <String>]`: Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="0e433-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="0e433-144">`[AsyncOperationId <String>]`: Aszinkron műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="0e433-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="0e433-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0e433-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e433-146">`[Location <String>]`: Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0e433-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="0e433-147">`[QuotaName <String>]`: A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="0e433-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="0e433-148">`[ResourceGroup <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e433-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="0e433-149">`[ServiceName <String>]`: Storage Service Name (tárterület neve)</span><span class="sxs-lookup"><span data-stu-id="0e433-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="0e433-150">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0e433-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="0e433-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e433-151">RELATED LINKS</span></span>

