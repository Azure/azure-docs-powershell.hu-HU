---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: 707e7e4e702912d4d838913cb7ca030fef914e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164490"
---
# <span data-ttu-id="856ee-101">Get-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="856ee-101">Get-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="856ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="856ee-102">SYNOPSIS</span></span>
<span data-ttu-id="856ee-103">Privát felhő</span><span class="sxs-lookup"><span data-stu-id="856ee-103">Get a private cloud</span></span>

## <span data-ttu-id="856ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="856ee-104">SYNTAX</span></span>

### <span data-ttu-id="856ee-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="856ee-105">List1 (Default)</span></span>
```
Get-AzVMwarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="856ee-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="856ee-106">Get</span></span>
```
Get-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="856ee-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="856ee-107">GetViaIdentity</span></span>
```
Get-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="856ee-108">Lista</span><span class="sxs-lookup"><span data-stu-id="856ee-108">List</span></span>
```
Get-AzVMwarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="856ee-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="856ee-109">DESCRIPTION</span></span>
<span data-ttu-id="856ee-110">Privát felhő</span><span class="sxs-lookup"><span data-stu-id="856ee-110">Get a private cloud</span></span>

## <span data-ttu-id="856ee-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="856ee-111">EXAMPLES</span></span>

### <span data-ttu-id="856ee-112">1. példa: Privát felhő felsorolása az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="856ee-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="856ee-113">Privát felhő listába sorolás az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="856ee-113">List private cloud under subscription</span></span>

### <span data-ttu-id="856ee-114">2. példa: A privát felhő felsorolása az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="856ee-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="856ee-115">Privát felhő listába sorolása az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="856ee-115">List private cloud under resource group</span></span>

### <span data-ttu-id="856ee-116">3. példa: Privát felhő</span><span class="sxs-lookup"><span data-stu-id="856ee-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="856ee-117">Privát felhőbe való beszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="856ee-117">Get private cloud</span></span>

## <span data-ttu-id="856ee-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="856ee-118">PARAMETERS</span></span>

### <span data-ttu-id="856ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856ee-119">-DefaultProfile</span></span>
<span data-ttu-id="856ee-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="856ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="856ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="856ee-121">-InputObject</span></span>
<span data-ttu-id="856ee-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="856ee-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="856ee-123">-Name</span><span class="sxs-lookup"><span data-stu-id="856ee-123">-Name</span></span>
<span data-ttu-id="856ee-124">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="856ee-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="856ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="856ee-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="856ee-126">The name of the resource group.</span></span>
<span data-ttu-id="856ee-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="856ee-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="856ee-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="856ee-128">-SubscriptionId</span></span>
<span data-ttu-id="856ee-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="856ee-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="856ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856ee-130">CommonParameters</span></span>
<span data-ttu-id="856ee-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856ee-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="856ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856ee-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="856ee-133">INPUTS</span></span>

### <span data-ttu-id="856ee-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="856ee-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="856ee-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="856ee-135">OUTPUTS</span></span>

### <span data-ttu-id="856ee-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="856ee-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="856ee-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="856ee-137">NOTES</span></span>

<span data-ttu-id="856ee-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="856ee-138">ALIASES</span></span>

<span data-ttu-id="856ee-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="856ee-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="856ee-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="856ee-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="856ee-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="856ee-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="856ee-142">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="856ee-142">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="856ee-143">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="856ee-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="856ee-144">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="856ee-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="856ee-145">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="856ee-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="856ee-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="856ee-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="856ee-147">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="856ee-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="856ee-148">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="856ee-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="856ee-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="856ee-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="856ee-150">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="856ee-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="856ee-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="856ee-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="856ee-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="856ee-152">RELATED LINKS</span></span>

