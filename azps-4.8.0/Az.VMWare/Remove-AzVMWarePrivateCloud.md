---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182459"
---
# <span data-ttu-id="364d9-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="364d9-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="364d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="364d9-102">SYNOPSIS</span></span>
<span data-ttu-id="364d9-103">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="364d9-103">Delete a private cloud</span></span>

## <span data-ttu-id="364d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="364d9-104">SYNTAX</span></span>

### <span data-ttu-id="364d9-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="364d9-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="364d9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="364d9-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="364d9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="364d9-107">DESCRIPTION</span></span>
<span data-ttu-id="364d9-108">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="364d9-108">Delete a private cloud</span></span>

## <span data-ttu-id="364d9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="364d9-109">EXAMPLES</span></span>

### <span data-ttu-id="364d9-110">Példa 1: privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="364d9-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="364d9-111">Privát felhő törlése</span><span class="sxs-lookup"><span data-stu-id="364d9-111">Delete private cloud</span></span>

## <span data-ttu-id="364d9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="364d9-112">PARAMETERS</span></span>

### <span data-ttu-id="364d9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="364d9-113">-AsJob</span></span>
<span data-ttu-id="364d9-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="364d9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="364d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364d9-115">-DefaultProfile</span></span>
<span data-ttu-id="364d9-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="364d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364d9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="364d9-117">-InputObject</span></span>
<span data-ttu-id="364d9-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="364d9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="364d9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="364d9-119">-Name</span></span>
<span data-ttu-id="364d9-120">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="364d9-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364d9-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="364d9-121">-NoWait</span></span>
<span data-ttu-id="364d9-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="364d9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="364d9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="364d9-123">-PassThru</span></span>
<span data-ttu-id="364d9-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="364d9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="364d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="364d9-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="364d9-126">The name of the resource group.</span></span>
<span data-ttu-id="364d9-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="364d9-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="364d9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="364d9-128">-SubscriptionId</span></span>
<span data-ttu-id="364d9-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="364d9-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="364d9-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="364d9-130">-Confirm</span></span>
<span data-ttu-id="364d9-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="364d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364d9-132">-WhatIf</span></span>
<span data-ttu-id="364d9-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="364d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="364d9-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="364d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364d9-135">CommonParameters</span></span>
<span data-ttu-id="364d9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="364d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364d9-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="364d9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364d9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="364d9-138">INPUTS</span></span>

### <span data-ttu-id="364d9-139">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="364d9-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="364d9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="364d9-140">OUTPUTS</span></span>

### <span data-ttu-id="364d9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="364d9-141">System.Boolean</span></span>

## <span data-ttu-id="364d9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="364d9-142">NOTES</span></span>

<span data-ttu-id="364d9-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="364d9-143">ALIASES</span></span>

<span data-ttu-id="364d9-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="364d9-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="364d9-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="364d9-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="364d9-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="364d9-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="364d9-147">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="364d9-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="364d9-148">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="364d9-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="364d9-149">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="364d9-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="364d9-150">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="364d9-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="364d9-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="364d9-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="364d9-152">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="364d9-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="364d9-153">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="364d9-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="364d9-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="364d9-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="364d9-155">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="364d9-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="364d9-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="364d9-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="364d9-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="364d9-157">RELATED LINKS</span></span>

