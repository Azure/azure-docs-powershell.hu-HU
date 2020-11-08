---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017075"
---
# <span data-ttu-id="f03b6-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="f03b6-101">Get-AzsDisk</span></span>

## <span data-ttu-id="f03b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f03b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f03b6-103">A lemezt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f03b6-103">Returns the disk.</span></span>

## <span data-ttu-id="f03b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f03b6-104">SYNTAX</span></span>

### <span data-ttu-id="f03b6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f03b6-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f03b6-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f03b6-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f03b6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f03b6-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f03b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f03b6-108">DESCRIPTION</span></span>
<span data-ttu-id="f03b6-109">A lemezt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f03b6-109">Returns the disk.</span></span>

## <span data-ttu-id="f03b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f03b6-110">EXAMPLES</span></span>

### <span data-ttu-id="f03b6-111">Példa 1: az összes lemez beolvasása</span><span class="sxs-lookup"><span data-stu-id="f03b6-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="f03b6-112">Paraméterek nélkül a `Get-AzsDisk` program felsorolja az összes lemezt.</span><span class="sxs-lookup"><span data-stu-id="f03b6-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="f03b6-113">2. példa: lemez beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="f03b6-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="f03b6-114">Adjon meg egy lemezt a `Name` lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="f03b6-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="f03b6-115">3. példa: megadott számú lemez beszerzése</span><span class="sxs-lookup"><span data-stu-id="f03b6-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="f03b6-116">A `Count` megadott számú lemezek beolvasásához használja a paramétert.</span><span class="sxs-lookup"><span data-stu-id="f03b6-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="f03b6-117">Példa 4: az összes lemez beolvasása adott helyen</span><span class="sxs-lookup"><span data-stu-id="f03b6-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="f03b6-118">Az `ScaleUnit` vagy `VolumeLabel` paraméter használata adott helyen lévő összes lemez listázásához</span><span class="sxs-lookup"><span data-stu-id="f03b6-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="f03b6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f03b6-119">PARAMETERS</span></span>

### <span data-ttu-id="f03b6-120">-Count</span><span class="sxs-lookup"><span data-stu-id="f03b6-120">-Count</span></span>
<span data-ttu-id="f03b6-121">A visszaadni kívánt lemezek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="f03b6-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f03b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03b6-122">-DefaultProfile</span></span>
<span data-ttu-id="f03b6-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f03b6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03b6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f03b6-124">-InputObject</span></span>
<span data-ttu-id="f03b6-125">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f03b6-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f03b6-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="f03b6-126">-Location</span></span>
<span data-ttu-id="f03b6-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f03b6-127">Location of the resource.</span></span>

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

### <span data-ttu-id="f03b6-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f03b6-128">-Name</span></span>
<span data-ttu-id="f03b6-129">A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="f03b6-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f03b6-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="f03b6-130">-ScaleUnit</span></span>
<span data-ttu-id="f03b6-131">Az a méretarány, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="f03b6-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="f03b6-132">-MegosztásElérésiÚtja</span><span class="sxs-lookup"><span data-stu-id="f03b6-132">-SharePath</span></span>
<span data-ttu-id="f03b6-133">Az a megosztás, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="f03b6-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="f03b6-134">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="f03b6-134">-Start</span></span>
<span data-ttu-id="f03b6-135">A lekérdezett lemezek kezdési indexe.</span><span class="sxs-lookup"><span data-stu-id="f03b6-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f03b6-136">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f03b6-136">-Status</span></span>
<span data-ttu-id="f03b6-137">A Disk State paraméterei.</span><span class="sxs-lookup"><span data-stu-id="f03b6-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="f03b6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f03b6-138">-SubscriptionId</span></span>
<span data-ttu-id="f03b6-139">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="f03b6-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f03b6-140">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f03b6-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f03b6-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f03b6-141">-UserSubscriptionId</span></span>
<span data-ttu-id="f03b6-142">Az a felhasználói előfizetés azonosítója, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="f03b6-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="f03b6-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="f03b6-143">-VolumeLabel</span></span>
<span data-ttu-id="f03b6-144">Annak a kötetnek a Kötetcímke, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="f03b6-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="f03b6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03b6-145">CommonParameters</span></span>
<span data-ttu-id="f03b6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f03b6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03b6-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f03b6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03b6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f03b6-148">INPUTS</span></span>

### <span data-ttu-id="f03b6-149">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f03b6-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="f03b6-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f03b6-150">OUTPUTS</span></span>

### <span data-ttu-id="f03b6-151">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="f03b6-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="f03b6-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f03b6-152">NOTES</span></span>

<span data-ttu-id="f03b6-153">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f03b6-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f03b6-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f03b6-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f03b6-155">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f03b6-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f03b6-156">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="f03b6-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="f03b6-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f03b6-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f03b6-158">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f03b6-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f03b6-159">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="f03b6-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="f03b6-160">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f03b6-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="f03b6-161">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="f03b6-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="f03b6-162">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="f03b6-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f03b6-163">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="f03b6-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="f03b6-164">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="f03b6-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f03b6-165">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f03b6-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f03b6-166">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="f03b6-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="f03b6-167">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="f03b6-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="f03b6-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f03b6-168">RELATED LINKS</span></span>

