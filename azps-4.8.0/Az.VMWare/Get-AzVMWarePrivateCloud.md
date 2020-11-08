---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183439"
---
# <span data-ttu-id="a4617-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a4617-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="a4617-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4617-102">SYNOPSIS</span></span>
<span data-ttu-id="a4617-103">Privát felhő beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4617-103">Get a private cloud</span></span>

## <span data-ttu-id="a4617-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4617-104">SYNTAX</span></span>

### <span data-ttu-id="a4617-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4617-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4617-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4617-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4617-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4617-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4617-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a4617-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4617-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4617-109">DESCRIPTION</span></span>
<span data-ttu-id="a4617-110">Privát felhő beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4617-110">Get a private cloud</span></span>

## <span data-ttu-id="a4617-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a4617-111">EXAMPLES</span></span>

### <span data-ttu-id="a4617-112">1. példa: privát felhő listázása az előfizetés csoportban</span><span class="sxs-lookup"><span data-stu-id="a4617-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="a4617-113">Privát felhő listázása az előfizetés csoportban</span><span class="sxs-lookup"><span data-stu-id="a4617-113">List private cloud under subscription</span></span>

### <span data-ttu-id="a4617-114">2. példa: magánjellegű felhő listázása az erőforráscsoport csoportban</span><span class="sxs-lookup"><span data-stu-id="a4617-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="a4617-115">Privát felhő listázása az erőforráscsoport csoportban</span><span class="sxs-lookup"><span data-stu-id="a4617-115">List private cloud under resource group</span></span>

### <span data-ttu-id="a4617-116">3. példa: személyes felhő beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4617-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="a4617-117">Személyes felhő beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4617-117">Get private cloud</span></span>

## <span data-ttu-id="a4617-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4617-118">PARAMETERS</span></span>

### <span data-ttu-id="a4617-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4617-119">-DefaultProfile</span></span>
<span data-ttu-id="a4617-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4617-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4617-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4617-121">-InputObject</span></span>
<span data-ttu-id="a4617-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4617-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4617-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4617-123">-Name</span></span>
<span data-ttu-id="a4617-124">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="a4617-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4617-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4617-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4617-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4617-126">The name of the resource group.</span></span>
<span data-ttu-id="a4617-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="a4617-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4617-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4617-128">-SubscriptionId</span></span>
<span data-ttu-id="a4617-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4617-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4617-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4617-130">CommonParameters</span></span>
<span data-ttu-id="a4617-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4617-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4617-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4617-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4617-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4617-133">INPUTS</span></span>

### <span data-ttu-id="a4617-134">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="a4617-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="a4617-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4617-135">OUTPUTS</span></span>

### <span data-ttu-id="a4617-136">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a4617-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="a4617-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4617-137">NOTES</span></span>

<span data-ttu-id="a4617-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a4617-138">ALIASES</span></span>

<span data-ttu-id="a4617-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a4617-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4617-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a4617-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4617-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a4617-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4617-142">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a4617-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4617-143">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="a4617-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="a4617-144">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="a4617-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="a4617-145">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="a4617-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="a4617-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a4617-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4617-147">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="a4617-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="a4617-148">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="a4617-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="a4617-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4617-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4617-150">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="a4617-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4617-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4617-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a4617-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4617-152">RELATED LINKS</span></span>

