---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467042"
---
# <span data-ttu-id="e657b-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e657b-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="e657b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e657b-102">SYNOPSIS</span></span>
<span data-ttu-id="e657b-103">Privát felhő frissítése</span><span class="sxs-lookup"><span data-stu-id="e657b-103">Update a private cloud</span></span>

## <span data-ttu-id="e657b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e657b-104">SYNTAX</span></span>

### <span data-ttu-id="e657b-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e657b-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e657b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e657b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e657b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e657b-107">DESCRIPTION</span></span>
<span data-ttu-id="e657b-108">Privát felhő frissítése</span><span class="sxs-lookup"><span data-stu-id="e657b-108">Update a private cloud</span></span>

## <span data-ttu-id="e657b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e657b-109">EXAMPLES</span></span>

### <span data-ttu-id="e657b-110">1. példa: A privát felhő méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="e657b-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="e657b-111">A privát felhő méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="e657b-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="e657b-112">2. példa: A privát felhő méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="e657b-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="e657b-113">A privát felhő méretének frissítése bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="e657b-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="e657b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e657b-114">PARAMETERS</span></span>

### <span data-ttu-id="e657b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e657b-115">-AsJob</span></span>
<span data-ttu-id="e657b-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e657b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e657b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e657b-117">-DefaultProfile</span></span>
<span data-ttu-id="e657b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e657b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e657b-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="e657b-119">-IdentitySource</span></span>
<span data-ttu-id="e657b-120">vCenter egyszeri bejelentkezést azonosító források létrehozásához lásd a NOTES szakaszt az IDENTITYSOURCE tulajdonságokhoz, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="e657b-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e657b-121">-InputObject</span></span>
<span data-ttu-id="e657b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e657b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="e657b-123">-Internet</span></span>
<span data-ttu-id="e657b-124">Az internetkapcsolat be van kapcsolva vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="e657b-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="e657b-125">-ManagementClusterSize</span></span>
<span data-ttu-id="e657b-126">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="e657b-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e657b-127">-Name</span></span>
<span data-ttu-id="e657b-128">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="e657b-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e657b-129">-NoWait</span></span>
<span data-ttu-id="e657b-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e657b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e657b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e657b-131">-ResourceGroupName</span></span>
<span data-ttu-id="e657b-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e657b-132">The name of the resource group.</span></span>
<span data-ttu-id="e657b-133">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e657b-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e657b-134">-SubscriptionId</span></span>
<span data-ttu-id="e657b-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e657b-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e657b-136">-Tag</span></span>
<span data-ttu-id="e657b-137">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="e657b-137">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e657b-138">-Confirm</span></span>
<span data-ttu-id="e657b-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e657b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e657b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e657b-140">-WhatIf</span></span>
<span data-ttu-id="e657b-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e657b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e657b-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e657b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e657b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e657b-143">CommonParameters</span></span>
<span data-ttu-id="e657b-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e657b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e657b-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e657b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e657b-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e657b-146">INPUTS</span></span>

### <span data-ttu-id="e657b-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="e657b-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="e657b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e657b-148">OUTPUTS</span></span>

### <span data-ttu-id="e657b-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e657b-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="e657b-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e657b-150">NOTES</span></span>

<span data-ttu-id="e657b-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e657b-151">ALIASES</span></span>

<span data-ttu-id="e657b-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e657b-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e657b-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e657b-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e657b-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e657b-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e657b-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Egyszeri bejelentkezés identitásforrások</span><span class="sxs-lookup"><span data-stu-id="e657b-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="e657b-156">`[Alias <String>]`: A tartomány Net LESZT.ISM-neve</span><span class="sxs-lookup"><span data-stu-id="e657b-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="e657b-157">`[BaseGroupDn <String>]`: A csoportok alap megkülönböztető neve</span><span class="sxs-lookup"><span data-stu-id="e657b-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="e657b-158">`[BaseUserDn <String>]`: A felhasználók alap megkülönböztető neve</span><span class="sxs-lookup"><span data-stu-id="e657b-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="e657b-159">`[Domain <String>]`: A tartomány DNS-neve</span><span class="sxs-lookup"><span data-stu-id="e657b-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="e657b-160">`[Name <String>]`: Az identitásforrás neve</span><span class="sxs-lookup"><span data-stu-id="e657b-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="e657b-161">`[Password <String>]`: Az Active Directory-felhasználó jelszava, minimális olvasási hozzáféréssel az alapDN-hez a felhasználók és a csoportok számára.</span><span class="sxs-lookup"><span data-stu-id="e657b-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="e657b-162">`[PrimaryServer <String>]`: Elsődleges kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="e657b-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="e657b-163">`[SecondaryServer <String>]`: Másodlagos kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="e657b-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="e657b-164">`[Ssl <SslEnum?>]`: AZ LDAP-kommunikáció védelme SSL-tanúsítvánnyal (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="e657b-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="e657b-165">`[Username <String>]`: Annak az Active Directory-felhasználónak az azonosítója, aki legalább olvasási hozzáféréssel rendelkezik az alapDN-hez a felhasználók és a csoportok számára</span><span class="sxs-lookup"><span data-stu-id="e657b-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="e657b-166">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e657b-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e657b-167">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="e657b-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e657b-168">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="e657b-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e657b-169">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="e657b-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e657b-170">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e657b-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e657b-171">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="e657b-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e657b-172">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="e657b-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e657b-173">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e657b-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e657b-174">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e657b-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="e657b-175">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e657b-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e657b-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e657b-176">RELATED LINKS</span></span>

