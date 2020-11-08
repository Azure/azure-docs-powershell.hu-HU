---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024023"
---
# <span data-ttu-id="23670-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="23670-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="23670-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23670-102">SYNOPSIS</span></span>
<span data-ttu-id="23670-103">Állomáslista frissítése</span><span class="sxs-lookup"><span data-stu-id="23670-103">Update a host pool.</span></span>

## <span data-ttu-id="23670-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23670-104">SYNTAX</span></span>

### <span data-ttu-id="23670-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23670-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23670-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="23670-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23670-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23670-107">DESCRIPTION</span></span>
<span data-ttu-id="23670-108">Állomáslista frissítése</span><span class="sxs-lookup"><span data-stu-id="23670-108">Update a host pool.</span></span>

## <span data-ttu-id="23670-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23670-109">EXAMPLES</span></span>

### <span data-ttu-id="23670-110">Példa 1: a Windows virtuális asztali HostPool frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="23670-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="23670-111">Ez a parancs frissíti egy erőforráscsoport Windows virtuális asztali HostPool.</span><span class="sxs-lookup"><span data-stu-id="23670-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="23670-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23670-112">PARAMETERS</span></span>

### <span data-ttu-id="23670-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="23670-113">-CustomRdpProperty</span></span>
<span data-ttu-id="23670-114">Az HostPool egyéni RDP-tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="23670-114">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23670-115">-DefaultProfile</span></span>
<span data-ttu-id="23670-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23670-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23670-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="23670-117">-Description</span></span>
<span data-ttu-id="23670-118">A HostPool leírása.</span><span class="sxs-lookup"><span data-stu-id="23670-118">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="23670-119">-FriendlyName</span></span>
<span data-ttu-id="23670-120">A HostPool rövid neve.</span><span class="sxs-lookup"><span data-stu-id="23670-120">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23670-121">-InputObject</span></span>
<span data-ttu-id="23670-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23670-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23670-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="23670-123">-LoadBalancerType</span></span>
<span data-ttu-id="23670-124">A terheléselosztó típusa.</span><span class="sxs-lookup"><span data-stu-id="23670-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="23670-125">-MaxSessionLimit</span></span>
<span data-ttu-id="23670-126">A HostPool maximális munkamenet-korlátja.</span><span class="sxs-lookup"><span data-stu-id="23670-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="23670-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23670-127">-Name</span></span>
<span data-ttu-id="23670-128">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="23670-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="23670-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="23670-130">A HostPool PersonalDesktopAssignment típusa.</span><span class="sxs-lookup"><span data-stu-id="23670-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="23670-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="23670-132">Az előnyben részesített alkalmazásobjektum-csoport típusa, alapértelmezett az asztali alkalmazás csoportba</span><span class="sxs-lookup"><span data-stu-id="23670-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="23670-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="23670-134">A regisztrációs token lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="23670-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="23670-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="23670-136">A jogkivonat alaphelyzetbe állításának típusa.</span><span class="sxs-lookup"><span data-stu-id="23670-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23670-137">-ResourceGroupName</span></span>
<span data-ttu-id="23670-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23670-138">The name of the resource group.</span></span>
<span data-ttu-id="23670-139">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="23670-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="23670-140">-Gyűrű</span><span class="sxs-lookup"><span data-stu-id="23670-140">-Ring</span></span>
<span data-ttu-id="23670-141">A HostPool csengetési száma.</span><span class="sxs-lookup"><span data-stu-id="23670-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="23670-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="23670-142">-SsoContext</span></span>
<span data-ttu-id="23670-143">A ssoContext titkos kulcsát tartalmazó elérési út.</span><span class="sxs-lookup"><span data-stu-id="23670-143">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23670-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23670-144">-SubscriptionId</span></span>
<span data-ttu-id="23670-145">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="23670-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="23670-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="23670-146">-Tag</span></span>
<span data-ttu-id="23670-147">frissítendő Címkék</span><span class="sxs-lookup"><span data-stu-id="23670-147">tags to be updated</span></span>

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

### <span data-ttu-id="23670-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="23670-148">-ValidationEnvironment</span></span>
<span data-ttu-id="23670-149">Az érvényesítési környezet.</span><span class="sxs-lookup"><span data-stu-id="23670-149">Is validation environment.</span></span>

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

### <span data-ttu-id="23670-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23670-150">-Confirm</span></span>
<span data-ttu-id="23670-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23670-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23670-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23670-152">-WhatIf</span></span>
<span data-ttu-id="23670-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23670-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23670-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23670-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23670-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23670-155">CommonParameters</span></span>
<span data-ttu-id="23670-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23670-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23670-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23670-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23670-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23670-158">INPUTS</span></span>

### <span data-ttu-id="23670-159">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="23670-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="23670-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23670-160">OUTPUTS</span></span>

### <span data-ttu-id="23670-161">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="23670-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="23670-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23670-162">NOTES</span></span>

<span data-ttu-id="23670-163">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="23670-163">ALIASES</span></span>

<span data-ttu-id="23670-164">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="23670-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23670-165">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="23670-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23670-166">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="23670-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23670-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="23670-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23670-168">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="23670-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="23670-169">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="23670-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="23670-170">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="23670-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="23670-171">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="23670-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="23670-172">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="23670-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23670-173">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23670-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="23670-174">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="23670-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="23670-175">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="23670-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="23670-176">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="23670-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="23670-177">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="23670-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="23670-178">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="23670-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="23670-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23670-179">RELATED LINKS</span></span>

