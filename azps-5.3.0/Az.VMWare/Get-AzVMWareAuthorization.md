---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382729"
---
# <span data-ttu-id="0efe6-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="0efe6-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="0efe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0efe6-102">SYNOPSIS</span></span>
<span data-ttu-id="0efe6-103">ExpressRoute-kapcsolat kapcsolati engedély kérése név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0efe6-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="0efe6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0efe6-104">SYNTAX</span></span>

### <span data-ttu-id="0efe6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0efe6-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0efe6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0efe6-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0efe6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0efe6-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0efe6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0efe6-108">DESCRIPTION</span></span>
<span data-ttu-id="0efe6-109">ExpressRoute-kapcsolat kapcsolati engedély kérése név szerint egy privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0efe6-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="0efe6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0efe6-110">EXAMPLES</span></span>

### <span data-ttu-id="0efe6-111">1. példa: Engedély kérése</span><span class="sxs-lookup"><span data-stu-id="0efe6-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="0efe6-112">Ez a parancsmag hitelesítést kap `azps-test-auth` a privát felhőben `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="0efe6-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="0efe6-113">2. példa: Listaengedélyezési</span><span class="sxs-lookup"><span data-stu-id="0efe6-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="0efe6-114">Ez a parancsmag felsorolja az `azps-test-auth` engedélyezést a privát felhőben `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="0efe6-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="0efe6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0efe6-115">PARAMETERS</span></span>

### <span data-ttu-id="0efe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efe6-116">-DefaultProfile</span></span>
<span data-ttu-id="0efe6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0efe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efe6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efe6-118">-InputObject</span></span>
<span data-ttu-id="0efe6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0efe6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0efe6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0efe6-120">-Name</span></span>
<span data-ttu-id="0efe6-121">Az ExpressRoute-kapcsolat kapcsolati engedélyének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0efe6-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efe6-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0efe6-122">-PrivateCloudName</span></span>
<span data-ttu-id="0efe6-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="0efe6-123">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efe6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efe6-124">-ResourceGroupName</span></span>
<span data-ttu-id="0efe6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0efe6-125">The name of the resource group.</span></span>
<span data-ttu-id="0efe6-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0efe6-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efe6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0efe6-127">-SubscriptionId</span></span>
<span data-ttu-id="0efe6-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0efe6-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0efe6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efe6-129">CommonParameters</span></span>
<span data-ttu-id="0efe6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efe6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efe6-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0efe6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efe6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0efe6-132">INPUTS</span></span>

### <span data-ttu-id="0efe6-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="0efe6-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="0efe6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0efe6-134">OUTPUTS</span></span>

### <span data-ttu-id="0efe6-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="0efe6-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="0efe6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0efe6-136">NOTES</span></span>

<span data-ttu-id="0efe6-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0efe6-137">ALIASES</span></span>

<span data-ttu-id="0efe6-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0efe6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0efe6-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0efe6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0efe6-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0efe6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0efe6-141">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0efe6-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0efe6-142">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0efe6-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0efe6-143">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="0efe6-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0efe6-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0efe6-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0efe6-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0efe6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0efe6-146">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="0efe6-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0efe6-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="0efe6-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0efe6-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0efe6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0efe6-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0efe6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0efe6-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0efe6-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0efe6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0efe6-151">RELATED LINKS</span></span>

