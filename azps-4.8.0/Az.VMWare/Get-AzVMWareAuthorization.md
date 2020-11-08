---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182012"
---
# <span data-ttu-id="afed5-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="afed5-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="afed5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afed5-102">SYNOPSIS</span></span>
<span data-ttu-id="afed5-103">ExpressRoute-áramkör engedélyezésének kérése privát Felhőbeli névvel</span><span class="sxs-lookup"><span data-stu-id="afed5-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="afed5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afed5-104">SYNTAX</span></span>

### <span data-ttu-id="afed5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="afed5-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="afed5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="afed5-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="afed5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="afed5-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="afed5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="afed5-108">DESCRIPTION</span></span>
<span data-ttu-id="afed5-109">ExpressRoute-áramkör engedélyezésének kérése privát Felhőbeli névvel</span><span class="sxs-lookup"><span data-stu-id="afed5-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="afed5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="afed5-110">EXAMPLES</span></span>

### <span data-ttu-id="afed5-111">Példa 1: Engedélyezés kérése</span><span class="sxs-lookup"><span data-stu-id="afed5-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="afed5-112">Ez a parancsmag a `azps-test-auth` privát felhőben kap engedélyt `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="afed5-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="afed5-113">2. példa: lista-engedélyezés</span><span class="sxs-lookup"><span data-stu-id="afed5-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="afed5-114">Ez a parancsmag a `azps-test-auth` privát felhő szerinti engedélyezést jeleníti meg `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="afed5-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="afed5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afed5-115">PARAMETERS</span></span>

### <span data-ttu-id="afed5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afed5-116">-DefaultProfile</span></span>
<span data-ttu-id="afed5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afed5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afed5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afed5-118">-InputObject</span></span>
<span data-ttu-id="afed5-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="afed5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="afed5-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afed5-120">-Name</span></span>
<span data-ttu-id="afed5-121">A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="afed5-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="afed5-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="afed5-122">-PrivateCloudName</span></span>
<span data-ttu-id="afed5-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="afed5-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="afed5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afed5-124">-ResourceGroupName</span></span>
<span data-ttu-id="afed5-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="afed5-125">The name of the resource group.</span></span>
<span data-ttu-id="afed5-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="afed5-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="afed5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afed5-127">-SubscriptionId</span></span>
<span data-ttu-id="afed5-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="afed5-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="afed5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afed5-129">CommonParameters</span></span>
<span data-ttu-id="afed5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afed5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afed5-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="afed5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afed5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afed5-132">INPUTS</span></span>

### <span data-ttu-id="afed5-133">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="afed5-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="afed5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afed5-134">OUTPUTS</span></span>

### <span data-ttu-id="afed5-135">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="afed5-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="afed5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afed5-136">NOTES</span></span>

<span data-ttu-id="afed5-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="afed5-137">ALIASES</span></span>

<span data-ttu-id="afed5-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="afed5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="afed5-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="afed5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afed5-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="afed5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="afed5-141">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="afed5-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="afed5-142">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="afed5-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="afed5-143">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="afed5-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="afed5-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="afed5-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="afed5-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="afed5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="afed5-146">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="afed5-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="afed5-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="afed5-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="afed5-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="afed5-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="afed5-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="afed5-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="afed5-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="afed5-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="afed5-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afed5-151">RELATED LINKS</span></span>

