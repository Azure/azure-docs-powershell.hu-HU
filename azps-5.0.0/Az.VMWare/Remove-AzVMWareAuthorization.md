---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187901"
---
# <span data-ttu-id="44c93-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="44c93-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="44c93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44c93-102">SYNOPSIS</span></span>
<span data-ttu-id="44c93-103">ExpressRoute-áramkör engedélyezésének törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="44c93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44c93-104">SYNTAX</span></span>

### <span data-ttu-id="44c93-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44c93-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44c93-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44c93-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44c93-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="44c93-107">DESCRIPTION</span></span>
<span data-ttu-id="44c93-108">ExpressRoute-áramkör engedélyezésének törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="44c93-109">Példák</span><span class="sxs-lookup"><span data-stu-id="44c93-109">EXAMPLES</span></span>

### <span data-ttu-id="44c93-110">Példa 1: privát felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="44c93-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="44c93-111">Személyes felhő engedélyének törlése</span><span class="sxs-lookup"><span data-stu-id="44c93-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="44c93-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44c93-112">PARAMETERS</span></span>

### <span data-ttu-id="44c93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44c93-113">-AsJob</span></span>
<span data-ttu-id="44c93-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="44c93-114">Run the command as a job</span></span>

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

### <span data-ttu-id="44c93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c93-115">-DefaultProfile</span></span>
<span data-ttu-id="44c93-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44c93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c93-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44c93-117">-InputObject</span></span>
<span data-ttu-id="44c93-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44c93-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44c93-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44c93-119">-Name</span></span>
<span data-ttu-id="44c93-120">A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c93-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="44c93-121">-NoWait</span></span>
<span data-ttu-id="44c93-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="44c93-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44c93-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44c93-123">-PassThru</span></span>
<span data-ttu-id="44c93-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="44c93-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44c93-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="44c93-125">-PrivateCloudName</span></span>
<span data-ttu-id="44c93-126">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="44c93-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="44c93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c93-127">-ResourceGroupName</span></span>
<span data-ttu-id="44c93-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44c93-128">The name of the resource group.</span></span>
<span data-ttu-id="44c93-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="44c93-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44c93-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44c93-130">-SubscriptionId</span></span>
<span data-ttu-id="44c93-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44c93-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44c93-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44c93-132">-Confirm</span></span>
<span data-ttu-id="44c93-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44c93-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c93-134">-WhatIf</span></span>
<span data-ttu-id="44c93-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44c93-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c93-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44c93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c93-137">CommonParameters</span></span>
<span data-ttu-id="44c93-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44c93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c93-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44c93-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c93-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44c93-140">INPUTS</span></span>

### <span data-ttu-id="44c93-141">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="44c93-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="44c93-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44c93-142">OUTPUTS</span></span>

### <span data-ttu-id="44c93-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44c93-143">System.Boolean</span></span>

## <span data-ttu-id="44c93-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44c93-144">NOTES</span></span>

<span data-ttu-id="44c93-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="44c93-145">ALIASES</span></span>

<span data-ttu-id="44c93-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="44c93-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44c93-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="44c93-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44c93-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="44c93-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44c93-149">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="44c93-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44c93-150">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="44c93-151">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="44c93-152">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="44c93-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="44c93-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="44c93-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44c93-154">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="44c93-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="44c93-155">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="44c93-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="44c93-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44c93-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="44c93-157">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="44c93-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="44c93-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44c93-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="44c93-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44c93-159">RELATED LINKS</span></span>

