---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: d90c81e307d56272fb9808760ef969705decb5d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925697"
---
# <span data-ttu-id="aedc4-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="aedc4-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="aedc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aedc4-102">SYNOPSIS</span></span>
<span data-ttu-id="aedc4-103">Állomáskészlet létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="aedc4-103">Create or update a host pool.</span></span>

## <span data-ttu-id="aedc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aedc4-104">SYNTAX</span></span>

### <span data-ttu-id="aedc4-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aedc4-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aedc4-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="aedc4-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aedc4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aedc4-107">DESCRIPTION</span></span>
<span data-ttu-id="aedc4-108">Állomáskészlet létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="aedc4-108">Create or update a host pool.</span></span>

## <span data-ttu-id="aedc4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aedc4-109">EXAMPLES</span></span>

### <span data-ttu-id="aedc4-110">1. példa: Windows Virtual Desktop HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="aedc4-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="aedc4-111">Ez a parancs létrehoz egy Windows Virtuális asztal Gazdasort egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="aedc4-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="aedc4-112">1. példa: Windows Virtual Desktop HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="aedc4-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="aedc4-113">Ez a parancs létrehoz egy Windows Virtuális asztal Gazdasort egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="aedc4-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="aedc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aedc4-114">PARAMETERS</span></span>

### <span data-ttu-id="aedc4-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="aedc4-115">-CustomRdpProperty</span></span>
<span data-ttu-id="aedc4-116">A HostPool egyéni rdp tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="aedc4-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedc4-117">-DefaultProfile</span></span>
<span data-ttu-id="aedc4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aedc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aedc4-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="aedc4-119">-Description</span></span>
<span data-ttu-id="aedc4-120">A HostPool leírása.</span><span class="sxs-lookup"><span data-stu-id="aedc4-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="aedc4-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="aedc4-122">Asztali alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="aedc4-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="aedc4-123">-ExpirationTime</span></span>
<span data-ttu-id="aedc4-124">A regisztrációs jogkivonat lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="aedc4-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="aedc4-125">-FriendlyName</span></span>
<span data-ttu-id="aedc4-126">A HostPool rövid neve.</span><span class="sxs-lookup"><span data-stu-id="aedc4-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="aedc4-127">-HostPoolType</span></span>
<span data-ttu-id="aedc4-128">HostPool type for desktop.</span><span class="sxs-lookup"><span data-stu-id="aedc4-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="aedc4-129">-LoadBalancerType</span></span>
<span data-ttu-id="aedc4-130">A terheléselegyenlő típusa.</span><span class="sxs-lookup"><span data-stu-id="aedc4-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-131">-Location</span><span class="sxs-lookup"><span data-stu-id="aedc4-131">-Location</span></span>
<span data-ttu-id="aedc4-132">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="aedc4-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="aedc4-133">-MaxSessionLimit</span></span>
<span data-ttu-id="aedc4-134">A HostPool maximális munkamenetkorlátja.</span><span class="sxs-lookup"><span data-stu-id="aedc4-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="aedc4-135">-Name</span></span>
<span data-ttu-id="aedc4-136">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="aedc4-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="aedc4-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="aedc4-138">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="aedc4-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="aedc4-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="aedc4-140">Az előnyben részesített alkalmazáscsoport típusa ( alapértelmezett beállítás asztali alkalmazáscsoport)</span><span class="sxs-lookup"><span data-stu-id="aedc4-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="aedc4-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="aedc4-142">A regisztrációs jogkivonat base64 kódolt karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="aedc4-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="aedc4-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="aedc4-144">A jogkivonat alaphelyzetbe állításának típusa.</span><span class="sxs-lookup"><span data-stu-id="aedc4-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aedc4-145">-ResourceGroupName</span></span>
<span data-ttu-id="aedc4-146">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aedc4-146">The name of the resource group.</span></span>
<span data-ttu-id="aedc4-147">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="aedc4-147">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-148">-Csengetés</span><span class="sxs-lookup"><span data-stu-id="aedc4-148">-Ring</span></span>
<span data-ttu-id="aedc4-149">A HostPool csengetőszáma.</span><span class="sxs-lookup"><span data-stu-id="aedc4-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="aedc4-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="aedc4-151">A WVD SSO-tanúsítványok aláírására használható ügyfél ADFS-kiszolgáló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="aedc4-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="aedc4-152">-SsoClientId</span></span>
<span data-ttu-id="aedc4-153">A WVD SSO-tanúsítványok kibocsátásához használt regisztrált függőben hagyatkozás ügyfélazonosítója.</span><span class="sxs-lookup"><span data-stu-id="aedc4-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="aedc4-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="aedc4-155">Az Azure KeyVault elérési útja, amely az ADFS-hez való kommunikációhoz használt titkos adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="aedc4-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="aedc4-156">-SsoContext</span></span>
<span data-ttu-id="aedc4-157">SsoContext-titkos tartalmú billentyűk elérési útja.</span><span class="sxs-lookup"><span data-stu-id="aedc4-157">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="aedc4-158">-SsoSecretType</span></span>
<span data-ttu-id="aedc4-159">Az egyetlen előjel típusa a Titkos típus típuson.</span><span class="sxs-lookup"><span data-stu-id="aedc4-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="aedc4-160">-StartVMOnConnect</span></span>
<span data-ttu-id="aedc4-161">A StartVMOnConnect funkció be- és kikapcsolása.</span><span class="sxs-lookup"><span data-stu-id="aedc4-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aedc4-162">-SubscriptionId</span></span>
<span data-ttu-id="aedc4-163">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aedc4-163">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="aedc4-164">-Tag</span></span>
<span data-ttu-id="aedc4-165">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="aedc4-165">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="aedc4-166">-ValidationEnvironment</span></span>
<span data-ttu-id="aedc4-167">Érvényesítési környezet.</span><span class="sxs-lookup"><span data-stu-id="aedc4-167">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="aedc4-168">-VMTemplate</span></span>
<span data-ttu-id="aedc4-169">VM-sablon a sessionhosts konfigurációhoz a hostpoolon belül.</span><span class="sxs-lookup"><span data-stu-id="aedc4-169">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aedc4-170">-WorkspaceName</span></span>
<span data-ttu-id="aedc4-171">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="aedc4-171">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc4-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aedc4-172">-Confirm</span></span>
<span data-ttu-id="aedc4-173">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aedc4-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aedc4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aedc4-174">-WhatIf</span></span>
<span data-ttu-id="aedc4-175">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aedc4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aedc4-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aedc4-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aedc4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedc4-177">CommonParameters</span></span>
<span data-ttu-id="aedc4-178">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aedc4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedc4-179">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aedc4-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedc4-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aedc4-180">INPUTS</span></span>

## <span data-ttu-id="aedc4-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aedc4-181">OUTPUTS</span></span>

### <span data-ttu-id="aedc4-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.iHostPool</span><span class="sxs-lookup"><span data-stu-id="aedc4-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="aedc4-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aedc4-183">NOTES</span></span>

<span data-ttu-id="aedc4-184">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aedc4-184">ALIASES</span></span>

## <span data-ttu-id="aedc4-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aedc4-185">RELATED LINKS</span></span>

