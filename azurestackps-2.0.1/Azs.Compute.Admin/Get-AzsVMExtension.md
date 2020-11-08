---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015372"
---
# <span data-ttu-id="e01cb-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="e01cb-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="e01cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e01cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e01cb-103">Visszaadja a kért virtuálisgép-bővítményt a Publisherhez, írja be a verziószámot.</span><span class="sxs-lookup"><span data-stu-id="e01cb-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="e01cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e01cb-104">SYNTAX</span></span>

### <span data-ttu-id="e01cb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e01cb-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e01cb-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e01cb-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e01cb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e01cb-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e01cb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e01cb-108">DESCRIPTION</span></span>
<span data-ttu-id="e01cb-109">Visszaadja a kért virtuálisgép-bővítményt a Publisherhez, írja be a verziószámot.</span><span class="sxs-lookup"><span data-stu-id="e01cb-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="e01cb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e01cb-110">EXAMPLES</span></span>

### <span data-ttu-id="e01cb-111">Példa 1: az összes VM-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="e01cb-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="e01cb-112">Ha az összes paramétert üresen hagyja, az összes VMExtensions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e01cb-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="e01cb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e01cb-113">PARAMETERS</span></span>

### <span data-ttu-id="e01cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01cb-114">-DefaultProfile</span></span>
<span data-ttu-id="e01cb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e01cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e01cb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e01cb-116">-InputObject</span></span>
<span data-ttu-id="e01cb-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e01cb-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e01cb-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e01cb-118">-Location</span></span>
<span data-ttu-id="e01cb-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e01cb-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e01cb-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e01cb-120">-Publisher</span></span>
<span data-ttu-id="e01cb-121">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="e01cb-121">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e01cb-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e01cb-122">-SubscriptionId</span></span>
<span data-ttu-id="e01cb-123">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="e01cb-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e01cb-124">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e01cb-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e01cb-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e01cb-125">-Type</span></span>
<span data-ttu-id="e01cb-126">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="e01cb-126">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e01cb-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e01cb-127">-Version</span></span>
<span data-ttu-id="e01cb-128">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="e01cb-128">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e01cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01cb-129">CommonParameters</span></span>
<span data-ttu-id="e01cb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e01cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01cb-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e01cb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01cb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e01cb-132">INPUTS</span></span>

### <span data-ttu-id="e01cb-133">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e01cb-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="e01cb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e01cb-134">OUTPUTS</span></span>

### <span data-ttu-id="e01cb-135">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="e01cb-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="e01cb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e01cb-136">NOTES</span></span>

<span data-ttu-id="e01cb-137">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e01cb-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e01cb-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e01cb-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e01cb-139">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e01cb-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e01cb-140">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="e01cb-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="e01cb-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e01cb-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e01cb-142">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e01cb-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e01cb-143">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="e01cb-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="e01cb-144">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="e01cb-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e01cb-145">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="e01cb-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="e01cb-146">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="e01cb-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e01cb-147">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="e01cb-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="e01cb-148">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="e01cb-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e01cb-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e01cb-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e01cb-150">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="e01cb-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="e01cb-151">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="e01cb-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="e01cb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e01cb-152">RELATED LINKS</span></span>

