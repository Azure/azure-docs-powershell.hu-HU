---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842641"
---
# <span data-ttu-id="66959-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="66959-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="66959-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66959-102">SYNOPSIS</span></span>
<span data-ttu-id="66959-103">Új platformot hoz létre a Publisherben, az ajánlatban, a SKU-ban és a verzióban.</span><span class="sxs-lookup"><span data-stu-id="66959-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="66959-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66959-104">SYNTAX</span></span>

### <span data-ttu-id="66959-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66959-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66959-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="66959-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66959-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66959-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66959-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66959-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66959-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="66959-109">DESCRIPTION</span></span>
<span data-ttu-id="66959-110">Új platformot hoz létre a Publisherben, az ajánlatban, a SKU-ban és a verzióban.</span><span class="sxs-lookup"><span data-stu-id="66959-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="66959-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66959-111">EXAMPLES</span></span>

### <span data-ttu-id="66959-112">Példa 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="66959-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="66959-113">Platform-kép hozzáadása a blob-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="66959-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="66959-114">Használja az a SasUri a PlatformImage helyének megadásához, vagy használjon nyilvánosan elérhető URL-címet.</span><span class="sxs-lookup"><span data-stu-id="66959-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="66959-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66959-115">PARAMETERS</span></span>

### <span data-ttu-id="66959-116">Exception. üzenet</span><span class="sxs-lookup"><span data-stu-id="66959-116">Exception.Message</span></span>
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

### <span data-ttu-id="66959-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="66959-117">-BillingPartNumber</span></span>
<span data-ttu-id="66959-118">A szoftver költségeinek kiszámlázására használt cikkszám.</span><span class="sxs-lookup"><span data-stu-id="66959-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-119">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="66959-119">-DataDisks</span></span>
<span data-ttu-id="66959-120">A platform képe által használt adatlemezek.</span><span class="sxs-lookup"><span data-stu-id="66959-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="66959-121">A kivitelezéshez tekintse meg a DATADISKS tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="66959-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66959-122">-DefaultProfile</span></span>
<span data-ttu-id="66959-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66959-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66959-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66959-124">-InputObject</span></span>
<span data-ttu-id="66959-125">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66959-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="66959-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="66959-126">-Location</span></span>
<span data-ttu-id="66959-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="66959-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="66959-128">-NewImage</span></span>
<span data-ttu-id="66959-129">Új platform kép létrehozásához használt paraméterek</span><span class="sxs-lookup"><span data-stu-id="66959-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="66959-130">A kivitelezéshez tekintse meg a NEWIMAGE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="66959-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="66959-131">-Várva</span><span class="sxs-lookup"><span data-stu-id="66959-131">-NoWait</span></span>
<span data-ttu-id="66959-132">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="66959-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="66959-133">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="66959-133">-Offer</span></span>
<span data-ttu-id="66959-134">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="66959-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="66959-135">-OsType</span></span>
<span data-ttu-id="66959-136">Operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="66959-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="66959-137">-OsUri</span></span>
<span data-ttu-id="66959-138">A lemez helye.</span><span class="sxs-lookup"><span data-stu-id="66959-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="66959-139">-ProvisioningState</span></span>
<span data-ttu-id="66959-140">A platform képének kiépítési állapota</span><span class="sxs-lookup"><span data-stu-id="66959-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="66959-141">-Publisher</span></span>
<span data-ttu-id="66959-142">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="66959-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="66959-143">-Sku</span></span>
<span data-ttu-id="66959-144">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="66959-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66959-145">-SubscriptionId</span></span>
<span data-ttu-id="66959-146">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="66959-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66959-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="66959-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-148">-Verzió</span><span class="sxs-lookup"><span data-stu-id="66959-148">-Version</span></span>
<span data-ttu-id="66959-149">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="66959-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66959-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66959-150">-Confirm</span></span>
<span data-ttu-id="66959-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66959-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66959-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66959-152">-WhatIf</span></span>
<span data-ttu-id="66959-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66959-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66959-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66959-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="66959-155">Exception. üzenet</span><span class="sxs-lookup"><span data-stu-id="66959-155">Exception.Message</span></span>

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

### <span data-ttu-id="66959-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66959-156">CommonParameters</span></span>
<span data-ttu-id="66959-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66959-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66959-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66959-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66959-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66959-159">INPUTS</span></span>

### <span data-ttu-id="66959-160">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="66959-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="66959-161">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="66959-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="66959-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66959-162">OUTPUTS</span></span>

### <span data-ttu-id="66959-163">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="66959-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="66959-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66959-164">NOTES</span></span>

<span data-ttu-id="66959-165">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="66959-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66959-166">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="66959-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="66959-167">DATADISKS <IDataDisk [] >: a platform képe által használt adatlemezek.</span><span class="sxs-lookup"><span data-stu-id="66959-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="66959-168">`[Lun <Int32?>]`: Logikai egység száma</span><span class="sxs-lookup"><span data-stu-id="66959-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="66959-169">`[Uri <String>]`: A sablonfájl helye.</span><span class="sxs-lookup"><span data-stu-id="66959-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="66959-170">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="66959-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66959-171">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="66959-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="66959-172">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="66959-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66959-173">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="66959-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="66959-174">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="66959-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="66959-175">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="66959-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="66959-176">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="66959-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="66959-177">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="66959-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="66959-178">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="66959-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="66959-179">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="66959-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66959-180">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="66959-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="66959-181">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="66959-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="66959-182">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="66959-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="66959-183">NEWIMAGE <IPlatformImageParameters> : új platform kép létrehozásához használt paraméterek.</span><span class="sxs-lookup"><span data-stu-id="66959-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="66959-184">`[DataDisk <IDataDisk[]>]`: A platform képe által használt adatlemezek.</span><span class="sxs-lookup"><span data-stu-id="66959-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="66959-185">`[Lun <Int32?>]`: Logikai egység száma</span><span class="sxs-lookup"><span data-stu-id="66959-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="66959-186">`[Uri <String>]`: A sablonfájl helye.</span><span class="sxs-lookup"><span data-stu-id="66959-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="66959-187">`[DetailBillingPartNumber <String>]`: A szoftver költségeinek kiszámlázására használt cikkszám.</span><span class="sxs-lookup"><span data-stu-id="66959-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="66959-188">`[OSDiskOstype <OSType?>]`: Operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="66959-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="66959-189">`[OSDiskUri <String>]`: A lemez helye.</span><span class="sxs-lookup"><span data-stu-id="66959-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="66959-190">`[ProvisioningState <ProvisioningState?>]`: A platform kép kiépítési állapotát.</span><span class="sxs-lookup"><span data-stu-id="66959-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="66959-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66959-191">RELATED LINKS</span></span>

