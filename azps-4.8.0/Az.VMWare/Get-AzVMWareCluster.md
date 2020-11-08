---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017441"
---
# <span data-ttu-id="2e298-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="2e298-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="2e298-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e298-102">SYNOPSIS</span></span>
<span data-ttu-id="2e298-103">Fürt beszerzése név alapján privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="2e298-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e298-104">SYNTAX</span></span>

### <span data-ttu-id="2e298-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e298-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e298-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e298-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e298-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e298-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e298-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e298-108">DESCRIPTION</span></span>
<span data-ttu-id="2e298-109">Fürt beszerzése név alapján privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="2e298-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e298-110">EXAMPLES</span></span>

### <span data-ttu-id="2e298-111">1. példa: fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e298-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="2e298-112">Fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e298-112">Get cluster</span></span>

### <span data-ttu-id="2e298-113">2. példa: lista-fürtök</span><span class="sxs-lookup"><span data-stu-id="2e298-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="2e298-114">Kiszolgálófürtök listája</span><span class="sxs-lookup"><span data-stu-id="2e298-114">List clusters</span></span>

## <span data-ttu-id="2e298-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e298-115">PARAMETERS</span></span>

### <span data-ttu-id="2e298-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e298-116">-DefaultProfile</span></span>
<span data-ttu-id="2e298-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e298-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e298-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e298-118">-InputObject</span></span>
<span data-ttu-id="2e298-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e298-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e298-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e298-120">-Name</span></span>
<span data-ttu-id="2e298-121">A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="2e298-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2e298-122">-PrivateCloudName</span></span>
<span data-ttu-id="2e298-123">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="2e298-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="2e298-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e298-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e298-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e298-125">The name of the resource group.</span></span>
<span data-ttu-id="2e298-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="2e298-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2e298-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e298-127">-SubscriptionId</span></span>
<span data-ttu-id="2e298-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e298-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2e298-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e298-129">CommonParameters</span></span>
<span data-ttu-id="2e298-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e298-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e298-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e298-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e298-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e298-132">INPUTS</span></span>

### <span data-ttu-id="2e298-133">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2e298-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2e298-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e298-134">OUTPUTS</span></span>

### <span data-ttu-id="2e298-135">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="2e298-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="2e298-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e298-136">NOTES</span></span>

<span data-ttu-id="2e298-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2e298-137">ALIASES</span></span>

<span data-ttu-id="2e298-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="2e298-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e298-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2e298-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e298-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="2e298-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e298-141">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="2e298-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e298-142">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2e298-143">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2e298-144">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e298-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2e298-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2e298-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e298-146">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="2e298-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2e298-147">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="2e298-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2e298-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e298-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e298-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="2e298-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e298-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e298-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2e298-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e298-151">RELATED LINKS</span></span>

