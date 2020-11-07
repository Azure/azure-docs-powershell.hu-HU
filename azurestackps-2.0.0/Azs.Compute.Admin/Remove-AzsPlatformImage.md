---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844861"
---
# <span data-ttu-id="faa58-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="faa58-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="faa58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="faa58-102">SYNOPSIS</span></span>
<span data-ttu-id="faa58-103">Platform képének törlése</span><span class="sxs-lookup"><span data-stu-id="faa58-103">Delete a platform image</span></span>

## <span data-ttu-id="faa58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="faa58-104">SYNTAX</span></span>

### <span data-ttu-id="faa58-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="faa58-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="faa58-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="faa58-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faa58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="faa58-107">DESCRIPTION</span></span>
<span data-ttu-id="faa58-108">Platform képének törlése</span><span class="sxs-lookup"><span data-stu-id="faa58-108">Delete a platform image</span></span>

## <span data-ttu-id="faa58-109">Példák</span><span class="sxs-lookup"><span data-stu-id="faa58-109">EXAMPLES</span></span>

### <span data-ttu-id="faa58-110">Példa 1: platform képének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="faa58-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="faa58-111">Egy platformról származó kép eltávolításának sikeres felhívása nem ad eredményül semmilyen kimenetet</span><span class="sxs-lookup"><span data-stu-id="faa58-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="faa58-112">2. példa: platform képének eltávolítása: a nem létezik</span><span class="sxs-lookup"><span data-stu-id="faa58-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="faa58-113">A nem létező platformokat tartalmazó képek sikeres hívása nem minden kimenetet ad vissza</span><span class="sxs-lookup"><span data-stu-id="faa58-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="faa58-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="faa58-114">PARAMETERS</span></span>

### <span data-ttu-id="faa58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa58-115">-DefaultProfile</span></span>
<span data-ttu-id="faa58-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faa58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa58-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa58-117">-InputObject</span></span>
<span data-ttu-id="faa58-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="faa58-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="faa58-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="faa58-119">-Location</span></span>
<span data-ttu-id="faa58-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="faa58-120">Location of the resource.</span></span>

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

### <span data-ttu-id="faa58-121">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="faa58-121">-Offer</span></span>
<span data-ttu-id="faa58-122">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-122">Name of the offer.</span></span>

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

### <span data-ttu-id="faa58-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faa58-123">-PassThru</span></span>
<span data-ttu-id="faa58-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="faa58-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="faa58-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="faa58-125">-Publisher</span></span>
<span data-ttu-id="faa58-126">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="faa58-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="faa58-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="faa58-127">-Sku</span></span>
<span data-ttu-id="faa58-128">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="faa58-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faa58-129">-SubscriptionId</span></span>
<span data-ttu-id="faa58-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="faa58-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="faa58-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="faa58-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="faa58-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="faa58-132">-Version</span></span>
<span data-ttu-id="faa58-133">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="faa58-133">The version of the resource.</span></span>

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

### <span data-ttu-id="faa58-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="faa58-134">-Confirm</span></span>
<span data-ttu-id="faa58-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="faa58-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa58-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa58-136">-WhatIf</span></span>
<span data-ttu-id="faa58-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="faa58-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa58-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="faa58-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa58-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa58-139">CommonParameters</span></span>
<span data-ttu-id="faa58-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="faa58-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa58-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="faa58-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa58-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="faa58-142">INPUTS</span></span>

### <span data-ttu-id="faa58-143">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="faa58-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="faa58-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faa58-144">OUTPUTS</span></span>

### <span data-ttu-id="faa58-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="faa58-145">System.Boolean</span></span>



## <span data-ttu-id="faa58-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="faa58-146">NOTES</span></span>

<span data-ttu-id="faa58-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="faa58-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="faa58-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="faa58-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="faa58-149">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="faa58-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="faa58-150">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="faa58-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="faa58-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="faa58-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="faa58-152">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="faa58-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="faa58-153">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="faa58-154">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="faa58-155">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="faa58-156">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="faa58-157">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="faa58-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="faa58-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="faa58-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="faa58-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="faa58-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="faa58-160">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="faa58-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="faa58-161">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="faa58-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="faa58-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faa58-162">RELATED LINKS</span></span>

