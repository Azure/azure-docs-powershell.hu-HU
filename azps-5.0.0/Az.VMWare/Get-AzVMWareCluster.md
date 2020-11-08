---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194151"
---
# <span data-ttu-id="32413-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="32413-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="32413-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32413-102">SYNOPSIS</span></span>
<span data-ttu-id="32413-103">Fürt beszerzése név alapján privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="32413-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32413-104">SYNTAX</span></span>

### <span data-ttu-id="32413-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32413-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32413-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="32413-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32413-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="32413-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="32413-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="32413-108">DESCRIPTION</span></span>
<span data-ttu-id="32413-109">Fürt beszerzése név alapján privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="32413-110">Példák</span><span class="sxs-lookup"><span data-stu-id="32413-110">EXAMPLES</span></span>

### <span data-ttu-id="32413-111">1. példa: fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="32413-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="32413-112">Fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="32413-112">Get cluster</span></span>

### <span data-ttu-id="32413-113">2. példa: lista-fürtök</span><span class="sxs-lookup"><span data-stu-id="32413-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="32413-114">Kiszolgálófürtök listája</span><span class="sxs-lookup"><span data-stu-id="32413-114">List clusters</span></span>

## <span data-ttu-id="32413-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32413-115">PARAMETERS</span></span>

### <span data-ttu-id="32413-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32413-116">-DefaultProfile</span></span>
<span data-ttu-id="32413-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32413-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32413-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32413-118">-InputObject</span></span>
<span data-ttu-id="32413-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32413-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32413-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32413-120">-Name</span></span>
<span data-ttu-id="32413-121">A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32413-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="32413-122">-PrivateCloudName</span></span>
<span data-ttu-id="32413-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="32413-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="32413-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32413-124">-ResourceGroupName</span></span>
<span data-ttu-id="32413-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32413-125">The name of the resource group.</span></span>
<span data-ttu-id="32413-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="32413-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="32413-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32413-127">-SubscriptionId</span></span>
<span data-ttu-id="32413-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32413-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="32413-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32413-129">CommonParameters</span></span>
<span data-ttu-id="32413-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32413-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32413-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32413-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32413-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32413-132">INPUTS</span></span>

### <span data-ttu-id="32413-133">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="32413-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="32413-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32413-134">OUTPUTS</span></span>

### <span data-ttu-id="32413-135">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="32413-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="32413-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32413-136">NOTES</span></span>

<span data-ttu-id="32413-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="32413-137">ALIASES</span></span>

<span data-ttu-id="32413-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="32413-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32413-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="32413-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32413-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="32413-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32413-141">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="32413-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32413-142">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="32413-143">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="32413-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="32413-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="32413-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="32413-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32413-146">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="32413-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="32413-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="32413-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="32413-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32413-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="32413-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="32413-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="32413-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32413-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="32413-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32413-151">RELATED LINKS</span></span>

