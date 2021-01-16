---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 724e1877b924829560112f926b75bd1c523c8f18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341418"
---
# <span data-ttu-id="d6a5e-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="d6a5e-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="d6a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a5e-103">Alkalmazás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-103">Create or update an application.</span></span>

## <span data-ttu-id="d6a5e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6a5e-104">SYNTAX</span></span>

### <span data-ttu-id="d6a5e-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6a5e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6a5e-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="d6a5e-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6a5e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6a5e-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a5e-108">Alkalmazás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-108">Create or update an application.</span></span>

## <span data-ttu-id="d6a5e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6a5e-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a5e-110">1. példa: Virtuális Windows-alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6a5e-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="d6a5e-111">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazást egy aplicaton groupban.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="d6a5e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6a5e-112">PARAMETERS</span></span>

### <span data-ttu-id="d6a5e-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="d6a5e-113">-AppAlias</span></span>
<span data-ttu-id="d6a5e-114">Alkalmazás aliasa a Start menüelemről</span><span class="sxs-lookup"><span data-stu-id="d6a5e-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="d6a5e-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="d6a5e-115">-ApplicationType</span></span>
<span data-ttu-id="d6a5e-116">Erőforrás típusa alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="d6a5e-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="d6a5e-117">-CommandLineArgument</span></span>
<span data-ttu-id="d6a5e-118">Az alkalmazás parancssori argumentumai.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="d6a5e-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="d6a5e-119">-CommandLineSetting</span></span>
<span data-ttu-id="d6a5e-120">Meghatározza, hogy elindítható-e ez a közzétett alkalmazás az ügyfél által megadott parancssori argumentumokkal, a közzétételkor megadott parancssori argumentumokkal vagy egyáltalán nem.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="d6a5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a5e-121">-DefaultProfile</span></span>
<span data-ttu-id="d6a5e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a5e-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d6a5e-123">-Description</span></span>
<span data-ttu-id="d6a5e-124">Az alkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-124">Description of Application.</span></span>

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

### <span data-ttu-id="d6a5e-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d6a5e-125">-FilePath</span></span>
<span data-ttu-id="d6a5e-126">Az alkalmazás végrehajtható fájlja elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="d6a5e-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d6a5e-127">-FriendlyName</span></span>
<span data-ttu-id="d6a5e-128">Az alkalmazás rövid neve.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="d6a5e-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d6a5e-129">-GroupName</span></span>
<span data-ttu-id="d6a5e-130">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d6a5e-130">The name of the application group</span></span>

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

### <span data-ttu-id="d6a5e-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="d6a5e-131">-IconIndex</span></span>
<span data-ttu-id="d6a5e-132">Az ikon indexe.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-132">Index of the icon.</span></span>

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

### <span data-ttu-id="d6a5e-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="d6a5e-133">-IconPath</span></span>
<span data-ttu-id="d6a5e-134">Elérési út ikon.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-134">Path to icon.</span></span>

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

### <span data-ttu-id="d6a5e-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="d6a5e-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="d6a5e-136">Az MSIX-alkalmazások csomagalkalmazás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="d6a5e-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="d6a5e-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="d6a5e-138">Az MSIX-alkalmazások csomagnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="d6a5e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d6a5e-139">-Name</span></span>
<span data-ttu-id="d6a5e-140">Az alkalmazás neve a megadott alkalmazáscsoportban</span><span class="sxs-lookup"><span data-stu-id="d6a5e-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="d6a5e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a5e-141">-ResourceGroupName</span></span>
<span data-ttu-id="d6a5e-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-142">The name of the resource group.</span></span>
<span data-ttu-id="d6a5e-143">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d6a5e-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6a5e-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="d6a5e-144">-ShowInPortal</span></span>
<span data-ttu-id="d6a5e-145">Azt adja meg, hogy a RemoteApp program az RD Web Access-kiszolgálón legyen-e.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="d6a5e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6a5e-146">-SubscriptionId</span></span>
<span data-ttu-id="d6a5e-147">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6a5e-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6a5e-148">-Confirm</span></span>
<span data-ttu-id="d6a5e-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a5e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a5e-150">-WhatIf</span></span>
<span data-ttu-id="d6a5e-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a5e-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a5e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a5e-153">CommonParameters</span></span>
<span data-ttu-id="d6a5e-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a5e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a5e-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6a5e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a5e-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6a5e-156">INPUTS</span></span>

## <span data-ttu-id="d6a5e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a5e-157">OUTPUTS</span></span>

### <span data-ttu-id="d6a5e-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="d6a5e-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="d6a5e-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6a5e-159">NOTES</span></span>

<span data-ttu-id="d6a5e-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d6a5e-160">ALIASES</span></span>

## <span data-ttu-id="d6a5e-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6a5e-161">RELATED LINKS</span></span>

