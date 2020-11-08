---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015275"
---
# <span data-ttu-id="766e7-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="766e7-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="766e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="766e7-102">SYNOPSIS</span></span>
<span data-ttu-id="766e7-103">A kért lemezvezérlő-áttelepítési feladatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="766e7-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="766e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="766e7-104">SYNTAX</span></span>

### <span data-ttu-id="766e7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="766e7-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="766e7-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="766e7-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="766e7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="766e7-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="766e7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="766e7-108">DESCRIPTION</span></span>
<span data-ttu-id="766e7-109">A kért lemezvezérlő-áttelepítési feladatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="766e7-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="766e7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="766e7-110">EXAMPLES</span></span>

### <span data-ttu-id="766e7-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="766e7-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="766e7-112">A távtárolású áttelepítési feladatok listáját jeleníti meg a helyi helyen.</span><span class="sxs-lookup"><span data-stu-id="766e7-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="766e7-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="766e7-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="766e7-114">Adott távtárolású áttelepítési feladat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="766e7-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="766e7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="766e7-115">PARAMETERS</span></span>

### <span data-ttu-id="766e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766e7-116">-DefaultProfile</span></span>
<span data-ttu-id="766e7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="766e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="766e7-118">-InputObject</span></span>
<span data-ttu-id="766e7-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="766e7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="766e7-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="766e7-120">-Location</span></span>
<span data-ttu-id="766e7-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="766e7-121">Location of the resource.</span></span>

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

### <span data-ttu-id="766e7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="766e7-122">-Name</span></span>
<span data-ttu-id="766e7-123">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="766e7-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="766e7-124">-Status</span></span>
<span data-ttu-id="766e7-125">A lemezvezérlő-áttelepítési feladat állapotának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="766e7-125">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="766e7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="766e7-126">-SubscriptionId</span></span>
<span data-ttu-id="766e7-127">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="766e7-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="766e7-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="766e7-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="766e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766e7-129">CommonParameters</span></span>
<span data-ttu-id="766e7-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="766e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766e7-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="766e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766e7-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="766e7-132">INPUTS</span></span>

### <span data-ttu-id="766e7-133">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="766e7-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="766e7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="766e7-134">OUTPUTS</span></span>

### <span data-ttu-id="766e7-135">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="766e7-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="766e7-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="766e7-136">NOTES</span></span>

<span data-ttu-id="766e7-137">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="766e7-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="766e7-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="766e7-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="766e7-139">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="766e7-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="766e7-140">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="766e7-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="766e7-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="766e7-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="766e7-142">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="766e7-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="766e7-143">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="766e7-144">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="766e7-145">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="766e7-146">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="766e7-147">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="766e7-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="766e7-148">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="766e7-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="766e7-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="766e7-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="766e7-150">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="766e7-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="766e7-151">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="766e7-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="766e7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="766e7-152">RELATED LINKS</span></span>

