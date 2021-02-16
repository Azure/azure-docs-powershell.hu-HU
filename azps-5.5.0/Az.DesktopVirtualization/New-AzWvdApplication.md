---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163674"
---
# <span data-ttu-id="fa54f-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="fa54f-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="fa54f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa54f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa54f-103">Alkalmazás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="fa54f-103">Create or update an application.</span></span>

## <span data-ttu-id="fa54f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa54f-104">SYNTAX</span></span>

### <span data-ttu-id="fa54f-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa54f-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa54f-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="fa54f-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa54f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa54f-107">DESCRIPTION</span></span>
<span data-ttu-id="fa54f-108">Alkalmazás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="fa54f-108">Create or update an application.</span></span>

## <span data-ttu-id="fa54f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa54f-109">EXAMPLES</span></span>

### <span data-ttu-id="fa54f-110">1. példa: Virtuális Windows-alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa54f-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="fa54f-111">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazást egy applicaton groupban.</span><span class="sxs-lookup"><span data-stu-id="fa54f-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="fa54f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa54f-112">PARAMETERS</span></span>

### <span data-ttu-id="fa54f-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="fa54f-113">-AppAlias</span></span>
<span data-ttu-id="fa54f-114">Alkalmazás aliasa a Start menüelemről</span><span class="sxs-lookup"><span data-stu-id="fa54f-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa54f-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="fa54f-115">-ApplicationType</span></span>
<span data-ttu-id="fa54f-116">Erőforrás típusa alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="fa54f-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa54f-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="fa54f-117">-CommandLineArgument</span></span>
<span data-ttu-id="fa54f-118">Az alkalmazás parancssori argumentumai.</span><span class="sxs-lookup"><span data-stu-id="fa54f-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="fa54f-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="fa54f-119">-CommandLineSetting</span></span>
<span data-ttu-id="fa54f-120">Meghatározza, hogy elindítható-e ez a közzétett alkalmazás az ügyfél által megadott parancssori argumentumokkal, a közzétételkor megadott parancssori argumentumokkal vagy egyáltalán nem.</span><span class="sxs-lookup"><span data-stu-id="fa54f-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa54f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa54f-121">-DefaultProfile</span></span>
<span data-ttu-id="fa54f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa54f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa54f-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fa54f-123">-Description</span></span>
<span data-ttu-id="fa54f-124">Az alkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="fa54f-124">Description of Application.</span></span>

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

### <span data-ttu-id="fa54f-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="fa54f-125">-FilePath</span></span>
<span data-ttu-id="fa54f-126">Az alkalmazás végrehajtható fájlja elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa54f-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="fa54f-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fa54f-127">-FriendlyName</span></span>
<span data-ttu-id="fa54f-128">Az alkalmazás rövid neve.</span><span class="sxs-lookup"><span data-stu-id="fa54f-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="fa54f-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="fa54f-129">-GroupName</span></span>
<span data-ttu-id="fa54f-130">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fa54f-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa54f-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="fa54f-131">-IconIndex</span></span>
<span data-ttu-id="fa54f-132">Az ikon indexe.</span><span class="sxs-lookup"><span data-stu-id="fa54f-132">Index of the icon.</span></span>

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

### <span data-ttu-id="fa54f-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="fa54f-133">-IconPath</span></span>
<span data-ttu-id="fa54f-134">Elérési út ikon.</span><span class="sxs-lookup"><span data-stu-id="fa54f-134">Path to icon.</span></span>

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

### <span data-ttu-id="fa54f-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="fa54f-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="fa54f-136">Az MSIX-alkalmazások csomagalkalmazás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa54f-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="fa54f-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="fa54f-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="fa54f-138">Az MSIX-alkalmazások csomagnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa54f-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="fa54f-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fa54f-139">-Name</span></span>
<span data-ttu-id="fa54f-140">Az alkalmazás neve a megadott alkalmazáscsoportban</span><span class="sxs-lookup"><span data-stu-id="fa54f-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa54f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa54f-141">-ResourceGroupName</span></span>
<span data-ttu-id="fa54f-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa54f-142">The name of the resource group.</span></span>
<span data-ttu-id="fa54f-143">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fa54f-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fa54f-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="fa54f-144">-ShowInPortal</span></span>
<span data-ttu-id="fa54f-145">Azt adja meg, hogy a RemoteApp program az RD Web Access-kiszolgálón legyen-e.</span><span class="sxs-lookup"><span data-stu-id="fa54f-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="fa54f-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa54f-146">-SubscriptionId</span></span>
<span data-ttu-id="fa54f-147">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fa54f-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fa54f-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa54f-148">-Confirm</span></span>
<span data-ttu-id="fa54f-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa54f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa54f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa54f-150">-WhatIf</span></span>
<span data-ttu-id="fa54f-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa54f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa54f-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa54f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa54f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa54f-153">CommonParameters</span></span>
<span data-ttu-id="fa54f-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa54f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa54f-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa54f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa54f-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa54f-156">INPUTS</span></span>

## <span data-ttu-id="fa54f-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa54f-157">OUTPUTS</span></span>

### <span data-ttu-id="fa54f-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="fa54f-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="fa54f-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa54f-159">NOTES</span></span>

<span data-ttu-id="fa54f-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fa54f-160">ALIASES</span></span>

## <span data-ttu-id="fa54f-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa54f-161">RELATED LINKS</span></span>

