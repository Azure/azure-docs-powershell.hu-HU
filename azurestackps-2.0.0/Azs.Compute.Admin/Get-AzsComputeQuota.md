---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844929"
---
# <span data-ttu-id="c4b7b-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c4b7b-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="c4b7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b7b-103">Szerezzen be egy meglévő számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="c4b7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4b7b-104">SYNTAX</span></span>

### <span data-ttu-id="c4b7b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4b7b-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b7b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4b7b-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4b7b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4b7b-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c4b7b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b7b-109">Szerezzen be egy meglévő számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="c4b7b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4b7b-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b7b-111">Példa 1: a számítási kvóták beolvasása</span><span class="sxs-lookup"><span data-stu-id="c4b7b-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="c4b7b-112">Az `Get-AzsComputeQuota` összes számítási kvóta listáját a paraméterek nélkül futtatva érheti el.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="c4b7b-113">2. példa: a kvóta kiszámítása név szerint</span><span class="sxs-lookup"><span data-stu-id="c4b7b-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="c4b7b-114">Adja meg a kvóta nevét a parancssorban egy adott kvóta beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="c4b7b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4b7b-115">PARAMETERS</span></span>

### <span data-ttu-id="c4b7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b7b-116">-DefaultProfile</span></span>
<span data-ttu-id="c4b7b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4b7b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4b7b-118">-InputObject</span></span>
<span data-ttu-id="c4b7b-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c4b7b-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="c4b7b-120">-Location</span></span>
<span data-ttu-id="c4b7b-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-121">Location of the resource.</span></span>

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

### <span data-ttu-id="c4b7b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4b7b-122">-Name</span></span>
<span data-ttu-id="c4b7b-123">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-123">Name of the quota.</span></span>

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

### <span data-ttu-id="c4b7b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4b7b-124">-SubscriptionId</span></span>
<span data-ttu-id="c4b7b-125">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4b7b-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4b7b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b7b-127">CommonParameters</span></span>
<span data-ttu-id="c4b7b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4b7b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b7b-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b7b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4b7b-130">INPUTS</span></span>

### <span data-ttu-id="c4b7b-131">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c4b7b-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c4b7b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4b7b-132">OUTPUTS</span></span>

### <span data-ttu-id="c4b7b-133">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="c4b7b-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="c4b7b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4b7b-134">NOTES</span></span>

<span data-ttu-id="c4b7b-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4b7b-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c4b7b-137">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c4b7b-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4b7b-138">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c4b7b-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c4b7b-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4b7b-140">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c4b7b-141">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c4b7b-142">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c4b7b-143">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c4b7b-144">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c4b7b-145">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c4b7b-146">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4b7b-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c4b7b-148">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c4b7b-149">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="c4b7b-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c4b7b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4b7b-150">RELATED LINKS</span></span>

