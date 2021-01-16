---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: a6c7572808184f3c83037932f45d36c7af3ff7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341070"
---
# <span data-ttu-id="9ab07-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="9ab07-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="9ab07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab07-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab07-103">Gazdakészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="9ab07-103">Update a host pool.</span></span>

## <span data-ttu-id="9ab07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ab07-104">SYNTAX</span></span>

### <span data-ttu-id="9ab07-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ab07-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9ab07-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9ab07-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ab07-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ab07-107">DESCRIPTION</span></span>
<span data-ttu-id="9ab07-108">Gazdakészlet frissítése</span><span class="sxs-lookup"><span data-stu-id="9ab07-108">Update a host pool.</span></span>

## <span data-ttu-id="9ab07-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ab07-109">EXAMPLES</span></span>

### <span data-ttu-id="9ab07-110">1. példa: A Windows Virtual Desktop HostPool frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="9ab07-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="9ab07-111">Ez a parancs frissíti a Windows Virtual Desktop HostPoolt egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9ab07-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="9ab07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ab07-112">PARAMETERS</span></span>

### <span data-ttu-id="9ab07-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="9ab07-113">-CustomRdpProperty</span></span>
<span data-ttu-id="9ab07-114">A HostPool egyéni rdp tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="9ab07-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="9ab07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab07-115">-DefaultProfile</span></span>
<span data-ttu-id="9ab07-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ab07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab07-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9ab07-117">-Description</span></span>
<span data-ttu-id="9ab07-118">A HostPool leírása.</span><span class="sxs-lookup"><span data-stu-id="9ab07-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="9ab07-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9ab07-119">-FriendlyName</span></span>
<span data-ttu-id="9ab07-120">A HostPool rövid neve.</span><span class="sxs-lookup"><span data-stu-id="9ab07-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="9ab07-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ab07-121">-InputObject</span></span>
<span data-ttu-id="9ab07-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9ab07-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ab07-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="9ab07-123">-LoadBalancerType</span></span>
<span data-ttu-id="9ab07-124">A terheléselegyenlő típusa.</span><span class="sxs-lookup"><span data-stu-id="9ab07-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="9ab07-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="9ab07-125">-MaxSessionLimit</span></span>
<span data-ttu-id="9ab07-126">A HostPool maximális munkamenetkorlátja.</span><span class="sxs-lookup"><span data-stu-id="9ab07-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="9ab07-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9ab07-127">-Name</span></span>
<span data-ttu-id="9ab07-128">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="9ab07-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="9ab07-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="9ab07-130">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="9ab07-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="9ab07-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="9ab07-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="9ab07-132">Az előnyben részesített alkalmazáscsoport típusa( alapértelmezett beállítás az asztali alkalmazáscsoportra)</span><span class="sxs-lookup"><span data-stu-id="9ab07-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="9ab07-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="9ab07-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="9ab07-134">A regisztrációs jogkivonat lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="9ab07-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="9ab07-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="9ab07-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="9ab07-136">A jogkivonat alaphelyzetbe állításának típusa.</span><span class="sxs-lookup"><span data-stu-id="9ab07-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="9ab07-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab07-137">-ResourceGroupName</span></span>
<span data-ttu-id="9ab07-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ab07-138">The name of the resource group.</span></span>
<span data-ttu-id="9ab07-139">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9ab07-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9ab07-140">-Csengetés</span><span class="sxs-lookup"><span data-stu-id="9ab07-140">-Ring</span></span>
<span data-ttu-id="9ab07-141">A HostPool csengetőszáma.</span><span class="sxs-lookup"><span data-stu-id="9ab07-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="9ab07-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="9ab07-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="9ab07-143">A WVD SSO-tanúsítványok aláírására használható ügyfél ADFS-kiszolgáló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="9ab07-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="9ab07-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="9ab07-144">-SsoClientId</span></span>
<span data-ttu-id="9ab07-145">A WVD SSO-tanúsítványok kibocsátásához használt regisztrált függőben hagyatkozás ügyfélazonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ab07-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="9ab07-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="9ab07-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="9ab07-147">Az Azure KeyVault elérési útja, amely az ADFS-hez való kommunikációhoz használt titkos adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ab07-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="9ab07-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="9ab07-148">-SsoContext</span></span>
<span data-ttu-id="9ab07-149">SsoContext-titkos tartalmú billentyűk elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9ab07-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="9ab07-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="9ab07-150">-SsoSecretType</span></span>
<span data-ttu-id="9ab07-151">Az egyetlen előjel típusa a Titkos típus típuson.</span><span class="sxs-lookup"><span data-stu-id="9ab07-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab07-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ab07-152">-SubscriptionId</span></span>
<span data-ttu-id="9ab07-153">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ab07-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9ab07-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ab07-154">-Tag</span></span>
<span data-ttu-id="9ab07-155">frissítend kell a címkéket</span><span class="sxs-lookup"><span data-stu-id="9ab07-155">tags to be updated</span></span>

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

### <span data-ttu-id="9ab07-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="9ab07-156">-ValidationEnvironment</span></span>
<span data-ttu-id="9ab07-157">Érvényesítési környezet.</span><span class="sxs-lookup"><span data-stu-id="9ab07-157">Is validation environment.</span></span>

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

### <span data-ttu-id="9ab07-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="9ab07-158">-VMTemplate</span></span>
<span data-ttu-id="9ab07-159">VM-sablon a sessionhosts konfigurációhoz a hostpoolon belül.</span><span class="sxs-lookup"><span data-stu-id="9ab07-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="9ab07-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ab07-160">-Confirm</span></span>
<span data-ttu-id="9ab07-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ab07-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab07-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab07-162">-WhatIf</span></span>
<span data-ttu-id="9ab07-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ab07-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab07-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ab07-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab07-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab07-165">CommonParameters</span></span>
<span data-ttu-id="9ab07-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab07-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab07-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ab07-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab07-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ab07-168">INPUTS</span></span>

### <span data-ttu-id="9ab07-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9ab07-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9ab07-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ab07-170">OUTPUTS</span></span>

### <span data-ttu-id="9ab07-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.iHostPool</span><span class="sxs-lookup"><span data-stu-id="9ab07-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="9ab07-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ab07-172">NOTES</span></span>

<span data-ttu-id="9ab07-173">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9ab07-173">ALIASES</span></span>

<span data-ttu-id="9ab07-174">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9ab07-174">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ab07-175">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9ab07-175">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ab07-176">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ab07-176">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ab07-177">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9ab07-177">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ab07-178">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-178">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9ab07-179">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="9ab07-179">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9ab07-180">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-180">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9ab07-181">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-181">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9ab07-182">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9ab07-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ab07-183">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="9ab07-183">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="9ab07-184">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ab07-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9ab07-185">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9ab07-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="9ab07-186">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="9ab07-186">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9ab07-187">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ab07-187">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9ab07-188">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-188">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9ab07-189">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="9ab07-189">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9ab07-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ab07-190">RELATED LINKS</span></span>

