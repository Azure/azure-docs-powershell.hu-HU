---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364277"
---
# <span data-ttu-id="2e4ff-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="2e4ff-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="2e4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4ff-103">Privát felhő</span><span class="sxs-lookup"><span data-stu-id="2e4ff-103">Get a private cloud</span></span>

## <span data-ttu-id="2e4ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e4ff-104">SYNTAX</span></span>

### <span data-ttu-id="2e4ff-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e4ff-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e4ff-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="2e4ff-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e4ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e4ff-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e4ff-108">Lista</span><span class="sxs-lookup"><span data-stu-id="2e4ff-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e4ff-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e4ff-109">DESCRIPTION</span></span>
<span data-ttu-id="2e4ff-110">Privát felhő</span><span class="sxs-lookup"><span data-stu-id="2e4ff-110">Get a private cloud</span></span>

## <span data-ttu-id="2e4ff-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e4ff-111">EXAMPLES</span></span>

### <span data-ttu-id="2e4ff-112">1. példa: Privát felhő felsorolása az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="2e4ff-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="2e4ff-113">Privát felhő listába sorolás az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="2e4ff-113">List private cloud under subscription</span></span>

### <span data-ttu-id="2e4ff-114">2. példa: A privát felhő felsorolása az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="2e4ff-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="2e4ff-115">Privát felhő listába sorolása az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="2e4ff-115">List private cloud under resource group</span></span>

### <span data-ttu-id="2e4ff-116">3. példa: Privát felhő</span><span class="sxs-lookup"><span data-stu-id="2e4ff-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="2e4ff-117">Privát felhő lekérte</span><span class="sxs-lookup"><span data-stu-id="2e4ff-117">Get private cloud</span></span>

## <span data-ttu-id="2e4ff-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e4ff-118">PARAMETERS</span></span>

### <span data-ttu-id="2e4ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4ff-119">-DefaultProfile</span></span>
<span data-ttu-id="2e4ff-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e4ff-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e4ff-121">-InputObject</span></span>
<span data-ttu-id="2e4ff-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e4ff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e4ff-123">-Name</span></span>
<span data-ttu-id="2e4ff-124">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="2e4ff-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="2e4ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e4ff-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-126">The name of the resource group.</span></span>
<span data-ttu-id="2e4ff-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="2e4ff-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2e4ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e4ff-128">-SubscriptionId</span></span>
<span data-ttu-id="2e4ff-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2e4ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4ff-130">CommonParameters</span></span>
<span data-ttu-id="2e4ff-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4ff-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e4ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4ff-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e4ff-133">INPUTS</span></span>

### <span data-ttu-id="2e4ff-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2e4ff-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2e4ff-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e4ff-135">OUTPUTS</span></span>

### <span data-ttu-id="2e4ff-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="2e4ff-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="2e4ff-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e4ff-137">NOTES</span></span>

<span data-ttu-id="2e4ff-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2e4ff-138">ALIASES</span></span>

<span data-ttu-id="2e4ff-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2e4ff-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e4ff-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e4ff-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e4ff-142">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2e4ff-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e4ff-143">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e4ff-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2e4ff-144">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="2e4ff-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2e4ff-145">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="2e4ff-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2e4ff-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2e4ff-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e4ff-147">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="2e4ff-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2e4ff-148">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="2e4ff-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2e4ff-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e4ff-150">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="2e4ff-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e4ff-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2e4ff-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e4ff-152">RELATED LINKS</span></span>

