---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015368"
---
# <span data-ttu-id="3f891-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3f891-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="3f891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f891-102">SYNOPSIS</span></span>
<span data-ttu-id="3f891-103">Töröl egy meglévő számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="3f891-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="3f891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f891-104">SYNTAX</span></span>

### <span data-ttu-id="3f891-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f891-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f891-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f891-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f891-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f891-107">DESCRIPTION</span></span>
<span data-ttu-id="3f891-108">Töröl egy meglévő számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="3f891-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="3f891-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3f891-109">EXAMPLES</span></span>

### <span data-ttu-id="3f891-110">1. példa: számítási kvóta eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3f891-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="3f891-111">A számítási kvóta eltávolításának sikeres felhívása nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="3f891-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="3f891-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f891-112">PARAMETERS</span></span>

### <span data-ttu-id="3f891-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f891-113">-DefaultProfile</span></span>
<span data-ttu-id="3f891-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f891-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f891-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f891-115">-InputObject</span></span>
<span data-ttu-id="3f891-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f891-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f891-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="3f891-117">-Location</span></span>
<span data-ttu-id="3f891-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="3f891-118">Location of the resource.</span></span>

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

### <span data-ttu-id="3f891-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f891-119">-Name</span></span>
<span data-ttu-id="3f891-120">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-120">Name of the quota.</span></span>

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

### <span data-ttu-id="3f891-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f891-121">-PassThru</span></span>
<span data-ttu-id="3f891-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="3f891-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3f891-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f891-123">-SubscriptionId</span></span>
<span data-ttu-id="3f891-124">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="3f891-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f891-125">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3f891-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f891-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f891-126">-Confirm</span></span>
<span data-ttu-id="3f891-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f891-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f891-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f891-128">-WhatIf</span></span>
<span data-ttu-id="3f891-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f891-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f891-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f891-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f891-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f891-131">CommonParameters</span></span>
<span data-ttu-id="3f891-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f891-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f891-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f891-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f891-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f891-134">INPUTS</span></span>

### <span data-ttu-id="3f891-135">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3f891-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3f891-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f891-136">OUTPUTS</span></span>

### <span data-ttu-id="3f891-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f891-137">System.Boolean</span></span>



## <span data-ttu-id="3f891-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f891-138">NOTES</span></span>

<span data-ttu-id="3f891-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3f891-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f891-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3f891-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f891-141">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3f891-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f891-142">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="3f891-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3f891-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3f891-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f891-144">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="3f891-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3f891-145">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3f891-146">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3f891-147">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3f891-148">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3f891-149">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="3f891-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3f891-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="3f891-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f891-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3f891-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3f891-152">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="3f891-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3f891-153">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="3f891-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3f891-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f891-154">RELATED LINKS</span></span>

