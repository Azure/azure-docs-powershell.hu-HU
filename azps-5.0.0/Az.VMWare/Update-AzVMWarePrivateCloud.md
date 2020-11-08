---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195644"
---
# <span data-ttu-id="7024e-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7024e-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="7024e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7024e-102">SYNOPSIS</span></span>
<span data-ttu-id="7024e-103">Privát felhő frissítése</span><span class="sxs-lookup"><span data-stu-id="7024e-103">Update a private cloud</span></span>

## <span data-ttu-id="7024e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7024e-104">SYNTAX</span></span>

### <span data-ttu-id="7024e-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7024e-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7024e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7024e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7024e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7024e-107">DESCRIPTION</span></span>
<span data-ttu-id="7024e-108">Privát felhő frissítése</span><span class="sxs-lookup"><span data-stu-id="7024e-108">Update a private cloud</span></span>

## <span data-ttu-id="7024e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7024e-109">EXAMPLES</span></span>

### <span data-ttu-id="7024e-110">Példa 1: a privát felhő méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="7024e-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7024e-111">A privát felhő méretének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="7024e-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="7024e-112">2. példa: a privát felhő adatbeviteli objektum szerinti méretének frissítése</span><span class="sxs-lookup"><span data-stu-id="7024e-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7024e-113">A privát felhő méretének frissítése beviteli objektum szerint</span><span class="sxs-lookup"><span data-stu-id="7024e-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="7024e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7024e-114">PARAMETERS</span></span>

### <span data-ttu-id="7024e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7024e-115">-AsJob</span></span>
<span data-ttu-id="7024e-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="7024e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7024e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7024e-117">-DefaultProfile</span></span>
<span data-ttu-id="7024e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7024e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7024e-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="7024e-119">-IdentitySource</span></span>
<span data-ttu-id="7024e-120">vCenter egyszeri bejelentkezéssel a kiépítéshez, lásd: IDENTITYSOURCE tulajdonságainak megjegyzések szakasza, és hozzon létre egy kivonatoló táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7024e-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7024e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7024e-121">-InputObject</span></span>
<span data-ttu-id="7024e-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7024e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7024e-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="7024e-123">-Internet</span></span>
<span data-ttu-id="7024e-124">Az internethez való csatlakozás engedélyezve van vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="7024e-124">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="7024e-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="7024e-125">-ManagementClusterSize</span></span>
<span data-ttu-id="7024e-126">A szektorcsoport mérete</span><span class="sxs-lookup"><span data-stu-id="7024e-126">The cluster size</span></span>

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

### <span data-ttu-id="7024e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7024e-127">-Name</span></span>
<span data-ttu-id="7024e-128">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="7024e-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="7024e-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="7024e-129">-NoWait</span></span>
<span data-ttu-id="7024e-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="7024e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7024e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7024e-131">-ResourceGroupName</span></span>
<span data-ttu-id="7024e-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7024e-132">The name of the resource group.</span></span>
<span data-ttu-id="7024e-133">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="7024e-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7024e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7024e-134">-SubscriptionId</span></span>
<span data-ttu-id="7024e-135">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7024e-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7024e-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="7024e-136">-Tag</span></span>
<span data-ttu-id="7024e-137">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="7024e-137">Resource tags.</span></span>

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

### <span data-ttu-id="7024e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7024e-138">-Confirm</span></span>
<span data-ttu-id="7024e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7024e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7024e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7024e-140">-WhatIf</span></span>
<span data-ttu-id="7024e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7024e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7024e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7024e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7024e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7024e-143">CommonParameters</span></span>
<span data-ttu-id="7024e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7024e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7024e-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7024e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7024e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7024e-146">INPUTS</span></span>

### <span data-ttu-id="7024e-147">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="7024e-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7024e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7024e-148">OUTPUTS</span></span>

### <span data-ttu-id="7024e-149">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7024e-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="7024e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7024e-150">NOTES</span></span>

<span data-ttu-id="7024e-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7024e-151">ALIASES</span></span>

<span data-ttu-id="7024e-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="7024e-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7024e-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7024e-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7024e-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7024e-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7024e-155">IDENTITYSOURCE <IIdentitySource [] >: vCenter egyszeri bejelentkezés az identitás forrásai között</span><span class="sxs-lookup"><span data-stu-id="7024e-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="7024e-156">`[Alias <String>]`: A tartomány NetBIOS-neve</span><span class="sxs-lookup"><span data-stu-id="7024e-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="7024e-157">`[BaseGroupDn <String>]`: A csoportok alapvető megkülönböztető neve</span><span class="sxs-lookup"><span data-stu-id="7024e-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="7024e-158">`[BaseUserDn <String>]`: A felhasználók alapvető megkülönböztető neve</span><span class="sxs-lookup"><span data-stu-id="7024e-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="7024e-159">`[Domain <String>]`: A tartomány DNS-neve</span><span class="sxs-lookup"><span data-stu-id="7024e-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="7024e-160">`[Name <String>]`: Az Identitáskezelő neve</span><span class="sxs-lookup"><span data-stu-id="7024e-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="7024e-161">`[Password <String>]`: Az Active Directory-felhasználó jelszava, legalább olvasási hozzáféréssel a felhasználók és a csoportok számára a bázis DN számára.</span><span class="sxs-lookup"><span data-stu-id="7024e-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="7024e-162">`[PrimaryServer <String>]`: Elsődleges kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="7024e-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="7024e-163">`[SecondaryServer <String>]`: A másodlagos kiszolgáló URL-címe</span><span class="sxs-lookup"><span data-stu-id="7024e-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="7024e-164">`[Ssl <SslEnum?>]`: LDAP-kommunikáció védelme SSL-tanúsítvánnyal (LDAP-szolgáltatással)</span><span class="sxs-lookup"><span data-stu-id="7024e-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="7024e-165">`[Username <String>]`: Egy Active Directory-felhasználó azonosítója, amelynek legalább olvasási hozzáférése van a felhasználóknak és a csoportoknak az Alap DN számára</span><span class="sxs-lookup"><span data-stu-id="7024e-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="7024e-166">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="7024e-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7024e-167">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7024e-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7024e-168">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7024e-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7024e-169">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7024e-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7024e-170">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7024e-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7024e-171">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="7024e-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7024e-172">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="7024e-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7024e-173">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7024e-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7024e-174">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="7024e-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="7024e-175">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7024e-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7024e-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7024e-176">RELATED LINKS</span></span>

