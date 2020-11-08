---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016622"
---
# <span data-ttu-id="359d8-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="359d8-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="359d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="359d8-102">SYNOPSIS</span></span>
<span data-ttu-id="359d8-103">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="359d8-103">Delete a quota by name.</span></span>

## <span data-ttu-id="359d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="359d8-104">SYNTAX</span></span>

### <span data-ttu-id="359d8-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="359d8-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="359d8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="359d8-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="359d8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="359d8-107">DESCRIPTION</span></span>
<span data-ttu-id="359d8-108">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="359d8-108">Delete a quota by name.</span></span>

## <span data-ttu-id="359d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="359d8-109">EXAMPLES</span></span>

### <span data-ttu-id="359d8-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="359d8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="359d8-111">Hálózati kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="359d8-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="359d8-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="359d8-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="359d8-113">Hálózati kvóta eltávolítása a pipe segítségével</span><span class="sxs-lookup"><span data-stu-id="359d8-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="359d8-114">PÉLDA--------------------------3--------------------------</span><span class="sxs-lookup"><span data-stu-id="359d8-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="359d8-115">Hálózati kvóta eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="359d8-115">Remove a network quota.</span></span>

## <span data-ttu-id="359d8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="359d8-116">PARAMETERS</span></span>

### <span data-ttu-id="359d8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="359d8-117">-AsJob</span></span>
<span data-ttu-id="359d8-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="359d8-118">Run the command as a job</span></span>

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

### <span data-ttu-id="359d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359d8-119">-DefaultProfile</span></span>
<span data-ttu-id="359d8-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="359d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="359d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="359d8-121">-InputObject</span></span>
<span data-ttu-id="359d8-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="359d8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="359d8-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="359d8-123">-Location</span></span>
<span data-ttu-id="359d8-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="359d8-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="359d8-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="359d8-125">-Name</span></span>
<span data-ttu-id="359d8-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="359d8-126">Name of the resource.</span></span>

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

### <span data-ttu-id="359d8-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="359d8-127">-NoWait</span></span>
<span data-ttu-id="359d8-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="359d8-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="359d8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="359d8-129">-PassThru</span></span>
<span data-ttu-id="359d8-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="359d8-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="359d8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="359d8-131">-SubscriptionId</span></span>
<span data-ttu-id="359d8-132">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="359d8-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="359d8-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="359d8-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="359d8-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="359d8-134">-Confirm</span></span>
<span data-ttu-id="359d8-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="359d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="359d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="359d8-136">-WhatIf</span></span>
<span data-ttu-id="359d8-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="359d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="359d8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="359d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="359d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359d8-139">CommonParameters</span></span>
<span data-ttu-id="359d8-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="359d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359d8-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="359d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359d8-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="359d8-142">INPUTS</span></span>

### <span data-ttu-id="359d8-143">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="359d8-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="359d8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="359d8-144">OUTPUTS</span></span>

### <span data-ttu-id="359d8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="359d8-145">System.Boolean</span></span>



## <span data-ttu-id="359d8-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="359d8-146">NOTES</span></span>

<span data-ttu-id="359d8-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="359d8-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="359d8-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="359d8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="359d8-149">INPUTOBJECT <INetworkAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="359d8-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="359d8-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="359d8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="359d8-151">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="359d8-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="359d8-152">`[ResourceName <String>]`: Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="359d8-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="359d8-153">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="359d8-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="359d8-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="359d8-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="359d8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="359d8-155">RELATED LINKS</span></span>

