---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017791"
---
# <span data-ttu-id="ded01-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="ded01-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="ded01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ded01-102">SYNOPSIS</span></span>
<span data-ttu-id="ded01-103">Állomáslista létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ded01-103">Create or update a host pool.</span></span>

## <span data-ttu-id="ded01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ded01-104">SYNTAX</span></span>

### <span data-ttu-id="ded01-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ded01-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ded01-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="ded01-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ded01-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ded01-107">DESCRIPTION</span></span>
<span data-ttu-id="ded01-108">Állomáslista létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ded01-108">Create or update a host pool.</span></span>

## <span data-ttu-id="ded01-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ded01-109">EXAMPLES</span></span>

### <span data-ttu-id="ded01-110">Példa 1: a Windows virtuális asztali HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="ded01-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="ded01-111">Ez a parancs létrehoz egy Windows virtuális asztali HostPool egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="ded01-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="ded01-112">Példa 1: a Windows virtuális asztali HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="ded01-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="ded01-113">Ez a parancs létrehoz egy Windows virtuális asztali HostPool egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="ded01-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="ded01-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ded01-114">PARAMETERS</span></span>

### <span data-ttu-id="ded01-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="ded01-115">-CustomRdpProperty</span></span>
<span data-ttu-id="ded01-116">Az HostPool egyéni RDP-tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="ded01-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="ded01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded01-117">-DefaultProfile</span></span>
<span data-ttu-id="ded01-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ded01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded01-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ded01-119">-Description</span></span>
<span data-ttu-id="ded01-120">A HostPool leírása.</span><span class="sxs-lookup"><span data-stu-id="ded01-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="ded01-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="ded01-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="ded01-122">Asztali app-csoport neve</span><span class="sxs-lookup"><span data-stu-id="ded01-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="ded01-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="ded01-123">-ExpirationTime</span></span>
<span data-ttu-id="ded01-124">A regisztrációs token lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="ded01-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="ded01-125">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="ded01-125">-FriendlyName</span></span>
<span data-ttu-id="ded01-126">A HostPool rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ded01-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="ded01-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="ded01-127">-HostPoolType</span></span>
<span data-ttu-id="ded01-128">HostPool típusa az asztalra.</span><span class="sxs-lookup"><span data-stu-id="ded01-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="ded01-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="ded01-129">-LoadBalancerType</span></span>
<span data-ttu-id="ded01-130">A terheléselosztó típusa.</span><span class="sxs-lookup"><span data-stu-id="ded01-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="ded01-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="ded01-131">-Location</span></span>
<span data-ttu-id="ded01-132">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="ded01-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ded01-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="ded01-133">-MaxSessionLimit</span></span>
<span data-ttu-id="ded01-134">A HostPool maximális munkamenet-korlátja.</span><span class="sxs-lookup"><span data-stu-id="ded01-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="ded01-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ded01-135">-Name</span></span>
<span data-ttu-id="ded01-136">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="ded01-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ded01-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="ded01-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="ded01-138">A HostPool PersonalDesktopAssignment típusa.</span><span class="sxs-lookup"><span data-stu-id="ded01-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="ded01-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="ded01-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="ded01-140">Az előnyben részesített alkalmazásobjektum-csoport típusa, alapértelmezett az asztali alkalmazás csoportba</span><span class="sxs-lookup"><span data-stu-id="ded01-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="ded01-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="ded01-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="ded01-142">A regisztrációs jogkivonat Base64 kódolt karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="ded01-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="ded01-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="ded01-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="ded01-144">A jogkivonat alaphelyzetbe állításának típusa.</span><span class="sxs-lookup"><span data-stu-id="ded01-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="ded01-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded01-145">-ResourceGroupName</span></span>
<span data-ttu-id="ded01-146">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ded01-146">The name of the resource group.</span></span>
<span data-ttu-id="ded01-147">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ded01-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ded01-148">-Gyűrű</span><span class="sxs-lookup"><span data-stu-id="ded01-148">-Ring</span></span>
<span data-ttu-id="ded01-149">A HostPool csengetési száma.</span><span class="sxs-lookup"><span data-stu-id="ded01-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="ded01-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="ded01-150">-SsoContext</span></span>
<span data-ttu-id="ded01-151">A ssoContext titkos kulcsát tartalmazó elérési út.</span><span class="sxs-lookup"><span data-stu-id="ded01-151">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="ded01-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ded01-152">-SubscriptionId</span></span>
<span data-ttu-id="ded01-153">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ded01-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ded01-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="ded01-154">-Tag</span></span>
<span data-ttu-id="ded01-155">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="ded01-155">Resource tags.</span></span>

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

### <span data-ttu-id="ded01-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="ded01-156">-ValidationEnvironment</span></span>
<span data-ttu-id="ded01-157">Az érvényesítési környezet.</span><span class="sxs-lookup"><span data-stu-id="ded01-157">Is validation environment.</span></span>

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

### <span data-ttu-id="ded01-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="ded01-158">-VMTemplate</span></span>
<span data-ttu-id="ded01-159">VM-sablon a sessionhosts-konfigurációhoz a hostpool belül.</span><span class="sxs-lookup"><span data-stu-id="ded01-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="ded01-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ded01-160">-WorkspaceName</span></span>
<span data-ttu-id="ded01-161">Munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="ded01-161">Workspace Name</span></span>

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

### <span data-ttu-id="ded01-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ded01-162">-Confirm</span></span>
<span data-ttu-id="ded01-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ded01-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded01-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded01-164">-WhatIf</span></span>
<span data-ttu-id="ded01-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ded01-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded01-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ded01-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded01-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded01-167">CommonParameters</span></span>
<span data-ttu-id="ded01-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ded01-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded01-169">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ded01-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded01-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ded01-170">INPUTS</span></span>

## <span data-ttu-id="ded01-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ded01-171">OUTPUTS</span></span>

### <span data-ttu-id="ded01-172">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="ded01-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="ded01-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ded01-173">NOTES</span></span>

<span data-ttu-id="ded01-174">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ded01-174">ALIASES</span></span>

## <span data-ttu-id="ded01-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ded01-175">RELATED LINKS</span></span>

