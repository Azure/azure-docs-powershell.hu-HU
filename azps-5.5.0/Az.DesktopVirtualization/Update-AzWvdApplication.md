---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209750"
---
# <span data-ttu-id="c7904-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="c7904-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="c7904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7904-102">SYNOPSIS</span></span>
<span data-ttu-id="c7904-103">Alkalmazás frissítése</span><span class="sxs-lookup"><span data-stu-id="c7904-103">Update an application.</span></span>

## <span data-ttu-id="c7904-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7904-104">SYNTAX</span></span>

### <span data-ttu-id="c7904-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7904-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7904-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7904-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7904-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7904-107">DESCRIPTION</span></span>
<span data-ttu-id="c7904-108">Alkalmazás frissítése</span><span class="sxs-lookup"><span data-stu-id="c7904-108">Update an application.</span></span>

## <span data-ttu-id="c7904-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7904-109">EXAMPLES</span></span>

### <span data-ttu-id="c7904-110">1. példa: Virtuális asztali Windows-alkalmazás frissítése</span><span class="sxs-lookup"><span data-stu-id="c7904-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="c7904-111">Ez a parancs egy applicaton-csoportban frissíti a Windows virtuális asztali alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="c7904-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="c7904-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7904-112">PARAMETERS</span></span>

### <span data-ttu-id="c7904-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="c7904-113">-ApplicationType</span></span>
<span data-ttu-id="c7904-114">Erőforrás típusa alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="c7904-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7904-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="c7904-115">-CommandLineArgument</span></span>
<span data-ttu-id="c7904-116">Alkalmazás parancssori argumentumai.</span><span class="sxs-lookup"><span data-stu-id="c7904-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="c7904-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="c7904-117">-CommandLineSetting</span></span>
<span data-ttu-id="c7904-118">Meghatározza, hogy elindítható-e ez a közzétett alkalmazás az ügyfél által megadott parancssori argumentumokkal, a közzétételkor megadott parancssori argumentumokkal vagy egyáltalán nem.</span><span class="sxs-lookup"><span data-stu-id="c7904-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7904-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7904-119">-DefaultProfile</span></span>
<span data-ttu-id="c7904-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7904-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7904-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c7904-121">-Description</span></span>
<span data-ttu-id="c7904-122">Az alkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="c7904-122">Description of Application.</span></span>

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

### <span data-ttu-id="c7904-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c7904-123">-FilePath</span></span>
<span data-ttu-id="c7904-124">Az alkalmazás végrehajtható fájlja elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7904-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="c7904-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c7904-125">-FriendlyName</span></span>
<span data-ttu-id="c7904-126">Az alkalmazás rövid neve.</span><span class="sxs-lookup"><span data-stu-id="c7904-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="c7904-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="c7904-127">-GroupName</span></span>
<span data-ttu-id="c7904-128">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c7904-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7904-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="c7904-129">-IconIndex</span></span>
<span data-ttu-id="c7904-130">Az ikon indexe.</span><span class="sxs-lookup"><span data-stu-id="c7904-130">Index of the icon.</span></span>

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

### <span data-ttu-id="c7904-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="c7904-131">-IconPath</span></span>
<span data-ttu-id="c7904-132">Elérési út ikon.</span><span class="sxs-lookup"><span data-stu-id="c7904-132">Path to icon.</span></span>

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

### <span data-ttu-id="c7904-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7904-133">-InputObject</span></span>
<span data-ttu-id="c7904-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c7904-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7904-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7904-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="c7904-136">Az MSIX-alkalmazások csomagalkalmazás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7904-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="c7904-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="c7904-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="c7904-138">Az MSIX-alkalmazások csomagnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7904-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="c7904-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c7904-139">-Name</span></span>
<span data-ttu-id="c7904-140">Az alkalmazás neve a megadott alkalmazáscsoportban</span><span class="sxs-lookup"><span data-stu-id="c7904-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7904-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7904-141">-ResourceGroupName</span></span>
<span data-ttu-id="c7904-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7904-142">The name of the resource group.</span></span>
<span data-ttu-id="c7904-143">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c7904-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7904-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="c7904-144">-ShowInPortal</span></span>
<span data-ttu-id="c7904-145">Azt adja meg, hogy a RemoteApp program az RD Web Access-kiszolgálón legyen-e.</span><span class="sxs-lookup"><span data-stu-id="c7904-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="c7904-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7904-146">-SubscriptionId</span></span>
<span data-ttu-id="c7904-147">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7904-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7904-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7904-148">-Tag</span></span>
<span data-ttu-id="c7904-149">frissítend kell a címkéket</span><span class="sxs-lookup"><span data-stu-id="c7904-149">tags to be updated</span></span>

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

### <span data-ttu-id="c7904-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7904-150">-Confirm</span></span>
<span data-ttu-id="c7904-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7904-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7904-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7904-152">-WhatIf</span></span>
<span data-ttu-id="c7904-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7904-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7904-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7904-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7904-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7904-155">CommonParameters</span></span>
<span data-ttu-id="c7904-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7904-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7904-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7904-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7904-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7904-158">INPUTS</span></span>

### <span data-ttu-id="c7904-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c7904-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c7904-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7904-160">OUTPUTS</span></span>

### <span data-ttu-id="c7904-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="c7904-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="c7904-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7904-162">NOTES</span></span>

<span data-ttu-id="c7904-163">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c7904-163">ALIASES</span></span>

<span data-ttu-id="c7904-164">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c7904-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7904-165">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c7904-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7904-166">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7904-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7904-167">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c7904-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7904-168">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c7904-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c7904-169">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="c7904-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c7904-170">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="c7904-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c7904-171">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="c7904-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c7904-172">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c7904-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7904-173">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="c7904-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c7904-174">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7904-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c7904-175">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c7904-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="c7904-176">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="c7904-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c7904-177">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7904-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c7904-178">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="c7904-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c7904-179">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="c7904-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c7904-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7904-180">RELATED LINKS</span></span>

