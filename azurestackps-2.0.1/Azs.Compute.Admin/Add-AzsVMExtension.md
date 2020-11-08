---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015341"
---
# <span data-ttu-id="fdbd7-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="fdbd7-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="fdbd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbd7-103">Virtuális számítógép-kiterjesztési kép létrehozása a Publisherrel, a verziószámmal</span><span class="sxs-lookup"><span data-stu-id="fdbd7-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="fdbd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdbd7-104">SYNTAX</span></span>

### <span data-ttu-id="fdbd7-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdbd7-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbd7-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdbd7-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbd7-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fdbd7-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fdbd7-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fdbd7-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fdbd7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdbd7-109">DESCRIPTION</span></span>
<span data-ttu-id="fdbd7-110">Virtuális számítógép-kiterjesztési kép létrehozása a Publisherrel, a verziószámmal</span><span class="sxs-lookup"><span data-stu-id="fdbd7-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="fdbd7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fdbd7-111">EXAMPLES</span></span>

### <span data-ttu-id="fdbd7-112">Példa 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="fdbd7-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="fdbd7-113">A nyilvánosan hozzáférhető hivatkozásra kattintva megadhatja a bővítmény helyét vagy az URI-azonosítót az Azure Blob-SasUri a segítségével.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="fdbd7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdbd7-114">PARAMETERS</span></span>

### <span data-ttu-id="fdbd7-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="fdbd7-115">-ComputeRole</span></span>
<span data-ttu-id="fdbd7-116">Számítási szerepkör</span><span class="sxs-lookup"><span data-stu-id="fdbd7-116">Compute role</span></span>

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

### <span data-ttu-id="fdbd7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd7-117">-DefaultProfile</span></span>
<span data-ttu-id="fdbd7-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdbd7-119">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="fdbd7-119">-Extension</span></span>
<span data-ttu-id="fdbd7-120">A virtuálisgép-bővítmények új lemezképének létrehozásához használt paraméterek</span><span class="sxs-lookup"><span data-stu-id="fdbd7-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="fdbd7-121">A kivitelezéshez a BŐVÍTMÉNYek tulajdonságairól szóló megjegyzések szakasz, és a kivonatoló táblázat létrehozása című témakörben talál további tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdbd7-122">-InputObject</span></span>
<span data-ttu-id="fdbd7-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdbd7-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="fdbd7-124">-IsSystemExtension</span></span>
<span data-ttu-id="fdbd7-125">Azt jelzi, hogy a kiterjesztés a rendszerhez van-e kijelölve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="fdbd7-126">-Location</span></span>
<span data-ttu-id="fdbd7-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-127">Location of the resource.</span></span>

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

### <span data-ttu-id="fdbd7-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="fdbd7-128">-PropertiesPublisher</span></span>
<span data-ttu-id="fdbd7-129">A VM-bővítmény kiadója</span><span class="sxs-lookup"><span data-stu-id="fdbd7-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="fdbd7-130">-ProvisioningState</span></span>
<span data-ttu-id="fdbd7-131">A kiterjesztés kiépítési állapota</span><span class="sxs-lookup"><span data-stu-id="fdbd7-131">Provisioning state of extension.</span></span>

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

### <span data-ttu-id="fdbd7-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fdbd7-132">-Publisher</span></span>
<span data-ttu-id="fdbd7-133">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="fdbd7-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="fdbd7-134">-SourceBlob</span></span>
<span data-ttu-id="fdbd7-135">URI – Azure vagy AzureStack blob.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-135">URI to Azure or AzureStack blob.</span></span>

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

### <span data-ttu-id="fdbd7-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdbd7-136">-SubscriptionId</span></span>
<span data-ttu-id="fdbd7-137">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fdbd7-138">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fdbd7-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="fdbd7-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="fdbd7-140">Igaz, ha támogatja a több bővítményt.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-141">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fdbd7-141">-Type</span></span>
<span data-ttu-id="fdbd7-142">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-142">Type of extension.</span></span>

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

### <span data-ttu-id="fdbd7-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="fdbd7-143">-Version</span></span>
<span data-ttu-id="fdbd7-144">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-144">The version of the resource.</span></span>

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

### <span data-ttu-id="fdbd7-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="fdbd7-145">-VmOsType</span></span>
<span data-ttu-id="fdbd7-146">A kiterjesztés-kezelő központi telepítéséhez szükséges cél a virtuális gép operációs rendszerének típusa.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="fdbd7-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="fdbd7-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="fdbd7-148">Az az érték, amely azt jelzi, hogy a bővítmény engedélyezve van-e a virtuálisgép-készlet támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fdbd7-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdbd7-149">-Confirm</span></span>
<span data-ttu-id="fdbd7-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbd7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbd7-151">-WhatIf</span></span>
<span data-ttu-id="fdbd7-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdbd7-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbd7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbd7-154">CommonParameters</span></span>
<span data-ttu-id="fdbd7-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdbd7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbd7-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbd7-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdbd7-157">INPUTS</span></span>

### <span data-ttu-id="fdbd7-158">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="fdbd7-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="fdbd7-159">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fdbd7-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="fdbd7-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdbd7-160">OUTPUTS</span></span>

### <span data-ttu-id="fdbd7-161">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="fdbd7-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="fdbd7-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdbd7-162">NOTES</span></span>

<span data-ttu-id="fdbd7-163">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fdbd7-164">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fdbd7-165">EXTENSION (kiterjesztés) <IVMExtensionParameters> : új virtuálisgép-bővítmény létrehozásakor használt paraméterek</span><span class="sxs-lookup"><span data-stu-id="fdbd7-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="fdbd7-166">`[ComputeRole <String>]`: Számítási szerepkör</span><span class="sxs-lookup"><span data-stu-id="fdbd7-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="fdbd7-167">`[IsSystemExtension <Boolean?>]`: Azt jelzi, hogy a kiterjesztés a rendszerhez van-e kijelölve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="fdbd7-168">`[ProvisioningState <ProvisioningState?>]`: A kiterjesztés kiépítési állapota.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="fdbd7-169">`[Publisher <String>]`: A VM-bővítmény kiadója</span><span class="sxs-lookup"><span data-stu-id="fdbd7-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="fdbd7-170">`[SourceBlobUri <String>]`: URI – Azure vagy AzureStack blob.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="fdbd7-171">`[SupportMultipleExtension <Boolean?>]`: Igaz, ha támogatja a több bővítményt.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="fdbd7-172">`[VMScaleSetEnabled <Boolean?>]`: Érték, amely azt jelzi, hogy a bővítmény engedélyezve van-e a virtuálisgép-készlet támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="fdbd7-173">`[VmosType <OSType?>]`: A bővítmény-kezelő központi telepítéséhez szükséges cél virtuális gép operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="fdbd7-174">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="fdbd7-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fdbd7-175">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="fdbd7-176">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="fdbd7-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fdbd7-177">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fdbd7-178">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="fdbd7-179">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="fdbd7-180">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="fdbd7-181">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="fdbd7-182">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="fdbd7-183">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fdbd7-184">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fdbd7-185">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="fdbd7-186">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="fdbd7-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="fdbd7-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdbd7-187">RELATED LINKS</span></span>

