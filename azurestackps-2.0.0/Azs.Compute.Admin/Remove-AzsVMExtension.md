---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844853"
---
# <span data-ttu-id="3e82e-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="3e82e-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="3e82e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e82e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e82e-103">Törli a virtuálisgép-bővítmény megadott képét.</span><span class="sxs-lookup"><span data-stu-id="3e82e-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="3e82e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e82e-104">SYNTAX</span></span>

### <span data-ttu-id="3e82e-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e82e-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e82e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e82e-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e82e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e82e-107">DESCRIPTION</span></span>
<span data-ttu-id="3e82e-108">Törli a virtuálisgép-bővítmény megadott képét.</span><span class="sxs-lookup"><span data-stu-id="3e82e-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="3e82e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3e82e-109">EXAMPLES</span></span>

### <span data-ttu-id="3e82e-110">Példa 1: létező VM-kiterjesztés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e82e-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="3e82e-111">A számítási kvóta eltávolításának sikeres felhívása nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="3e82e-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="3e82e-112">2. példa: nem létező VM-kiterjesztés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e82e-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="3e82e-113">A nem létező platformokat tartalmazó képek sikeres hívása nem minden kimenetet ad vissza</span><span class="sxs-lookup"><span data-stu-id="3e82e-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="3e82e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e82e-114">PARAMETERS</span></span>

### <span data-ttu-id="3e82e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e82e-115">-DefaultProfile</span></span>
<span data-ttu-id="3e82e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e82e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e82e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e82e-117">-InputObject</span></span>
<span data-ttu-id="3e82e-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e82e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e82e-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="3e82e-119">-Location</span></span>
<span data-ttu-id="3e82e-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="3e82e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3e82e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e82e-121">-PassThru</span></span>
<span data-ttu-id="3e82e-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="3e82e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3e82e-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3e82e-123">-Publisher</span></span>
<span data-ttu-id="3e82e-124">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="3e82e-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e82e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e82e-125">-SubscriptionId</span></span>
<span data-ttu-id="3e82e-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="3e82e-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e82e-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e82e-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e82e-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="3e82e-128">-Type</span></span>
<span data-ttu-id="3e82e-129">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="3e82e-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e82e-130">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3e82e-130">-Version</span></span>
<span data-ttu-id="3e82e-131">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="3e82e-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e82e-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e82e-132">-Confirm</span></span>
<span data-ttu-id="3e82e-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e82e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e82e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e82e-134">-WhatIf</span></span>
<span data-ttu-id="3e82e-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e82e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e82e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e82e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e82e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e82e-137">CommonParameters</span></span>
<span data-ttu-id="3e82e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e82e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e82e-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e82e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e82e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e82e-140">INPUTS</span></span>

### <span data-ttu-id="3e82e-141">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3e82e-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3e82e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e82e-142">OUTPUTS</span></span>

### <span data-ttu-id="3e82e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e82e-143">System.Boolean</span></span>



## <span data-ttu-id="3e82e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e82e-144">NOTES</span></span>

<span data-ttu-id="3e82e-145">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3e82e-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e82e-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3e82e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e82e-147">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3e82e-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e82e-148">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="3e82e-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3e82e-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3e82e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e82e-150">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="3e82e-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3e82e-151">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="3e82e-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3e82e-152">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="3e82e-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3e82e-153">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="3e82e-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3e82e-154">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="3e82e-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3e82e-155">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="3e82e-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3e82e-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="3e82e-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e82e-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e82e-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e82e-158">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="3e82e-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3e82e-159">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="3e82e-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3e82e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e82e-160">RELATED LINKS</span></span>

