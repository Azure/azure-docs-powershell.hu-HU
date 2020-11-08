---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017440"
---
# <span data-ttu-id="d47e6-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="d47e6-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="d47e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d47e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d47e6-103">Fürt törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="d47e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d47e6-104">SYNTAX</span></span>

### <span data-ttu-id="d47e6-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d47e6-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d47e6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d47e6-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d47e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d47e6-107">DESCRIPTION</span></span>
<span data-ttu-id="d47e6-108">Fürt törlése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="d47e6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d47e6-109">EXAMPLES</span></span>

### <span data-ttu-id="d47e6-110">Példa 1: fürt törlése a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="d47e6-111">Fürt törlése a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="d47e6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d47e6-112">PARAMETERS</span></span>

### <span data-ttu-id="d47e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d47e6-113">-AsJob</span></span>
<span data-ttu-id="d47e6-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d47e6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d47e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d47e6-115">-DefaultProfile</span></span>
<span data-ttu-id="d47e6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d47e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d47e6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d47e6-117">-InputObject</span></span>
<span data-ttu-id="d47e6-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d47e6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d47e6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d47e6-119">-Name</span></span>
<span data-ttu-id="d47e6-120">A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d47e6-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="d47e6-121">-NoWait</span></span>
<span data-ttu-id="d47e6-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d47e6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d47e6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d47e6-123">-PassThru</span></span>
<span data-ttu-id="d47e6-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d47e6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d47e6-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d47e6-125">-PrivateCloudName</span></span>
<span data-ttu-id="d47e6-126">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d47e6-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="d47e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d47e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d47e6-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d47e6-128">The name of the resource group.</span></span>
<span data-ttu-id="d47e6-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d47e6-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d47e6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d47e6-130">-SubscriptionId</span></span>
<span data-ttu-id="d47e6-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d47e6-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d47e6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d47e6-132">-Confirm</span></span>
<span data-ttu-id="d47e6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d47e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d47e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d47e6-134">-WhatIf</span></span>
<span data-ttu-id="d47e6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d47e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d47e6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d47e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d47e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d47e6-137">CommonParameters</span></span>
<span data-ttu-id="d47e6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d47e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d47e6-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d47e6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d47e6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d47e6-140">INPUTS</span></span>

### <span data-ttu-id="d47e6-141">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d47e6-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d47e6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d47e6-142">OUTPUTS</span></span>

### <span data-ttu-id="d47e6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d47e6-143">System.Boolean</span></span>

## <span data-ttu-id="d47e6-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d47e6-144">NOTES</span></span>

<span data-ttu-id="d47e6-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d47e6-145">ALIASES</span></span>

<span data-ttu-id="d47e6-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d47e6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d47e6-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d47e6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d47e6-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d47e6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d47e6-149">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d47e6-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d47e6-150">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d47e6-151">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d47e6-152">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d47e6-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d47e6-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d47e6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d47e6-154">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="d47e6-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d47e6-155">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d47e6-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d47e6-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d47e6-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d47e6-157">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d47e6-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d47e6-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d47e6-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d47e6-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d47e6-159">RELATED LINKS</span></span>

