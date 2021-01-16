---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357614"
---
# <span data-ttu-id="d012b-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d012b-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="d012b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d012b-102">SYNOPSIS</span></span>
<span data-ttu-id="d012b-103">MSIX-csomag létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d012b-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="d012b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d012b-104">SYNTAX</span></span>

### <span data-ttu-id="d012b-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d012b-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d012b-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="d012b-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d012b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d012b-107">DESCRIPTION</span></span>
<span data-ttu-id="d012b-108">MSIX-csomag létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d012b-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="d012b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d012b-109">EXAMPLES</span></span>

### <span data-ttu-id="d012b-110">1. példa: Új MSIX-csomag létrehozása a HostPoolban a Package Alias segítségével</span><span class="sxs-lookup"><span data-stu-id="d012b-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="d012b-111">Ez a parancs hozzáadja az MSIX-csomagot a megadott kép elérési útból a HostPoolhoz</span><span class="sxs-lookup"><span data-stu-id="d012b-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="d012b-112">2. példa: Új MSIX-csomag létrehozása a HostPoolban</span><span class="sxs-lookup"><span data-stu-id="d012b-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="d012b-113">Ez a parancs MSIX-csomagot ad hozzá a megadott HostPool-fájlhoz</span><span class="sxs-lookup"><span data-stu-id="d012b-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="d012b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d012b-114">PARAMETERS</span></span>

### <span data-ttu-id="d012b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d012b-115">-DefaultProfile</span></span>
<span data-ttu-id="d012b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d012b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d012b-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d012b-117">-DisplayName</span></span>
<span data-ttu-id="d012b-118">A portálon megjelenítendő felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="d012b-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="d012b-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="d012b-119">-FullName</span></span>
<span data-ttu-id="d012b-120">Az MSIX-csomag teljes neve a megadott állomáskészleten belül</span><span class="sxs-lookup"><span data-stu-id="d012b-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d012b-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d012b-121">-HostPoolName</span></span>
<span data-ttu-id="d012b-122">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="d012b-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d012b-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="d012b-123">-ImagePath</span></span>
<span data-ttu-id="d012b-124">VHD/CIM image path on Network Share.</span><span class="sxs-lookup"><span data-stu-id="d012b-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="d012b-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="d012b-125">-IsActive</span></span>
<span data-ttu-id="d012b-126">A csomagnak ez a verziója legyen aktív a gazdasoron.</span><span class="sxs-lookup"><span data-stu-id="d012b-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="d012b-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="d012b-127">-IsRegularRegistration</span></span>
<span data-ttu-id="d012b-128">Azt adja meg, hogy miként regisztrálja a Csomagot a hírcsatornában.</span><span class="sxs-lookup"><span data-stu-id="d012b-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="d012b-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="d012b-129">-LastUpdated</span></span>
<span data-ttu-id="d012b-130">Date Package was last updated, found in the appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="d012b-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="d012b-131">-PackageAlias</span></span>
<span data-ttu-id="d012b-132">Package Alias from extract MSIX Image</span><span class="sxs-lookup"><span data-stu-id="d012b-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d012b-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="d012b-133">-PackageApplication</span></span>
<span data-ttu-id="d012b-134">Csomagalkalmazások listája.</span><span class="sxs-lookup"><span data-stu-id="d012b-134">List of package applications.</span></span>

<span data-ttu-id="d012b-135">Ennek létrehozásáról a PACKAGEAPPLICATION tulajdonságokat és egy kivonattáblát hoz létre a MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="d012b-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d012b-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="d012b-136">-PackageDependency</span></span>
<span data-ttu-id="d012b-137">Csomagfüggőségek listája.</span><span class="sxs-lookup"><span data-stu-id="d012b-137">List of package dependencies.</span></span>

<span data-ttu-id="d012b-138">Ennek létrehozásáról a PACKAGEDEPENDENCY tulajdonságokat és a hash tábla létrehozásáról a NOTES (JEGYZETEK) című szakaszt lásd.</span><span class="sxs-lookup"><span data-stu-id="d012b-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d012b-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="d012b-139">-PackageFamilyName</span></span>
<span data-ttu-id="d012b-140">Csomag családneve a appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="d012b-141">Csomagnevet és Publisher-nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d012b-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="d012b-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="d012b-142">-PackageName</span></span>
<span data-ttu-id="d012b-143">Package Name from appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="d012b-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="d012b-144">-PackageRelativePath</span></span>
<span data-ttu-id="d012b-145">Relatív elérési út a képen belüli csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="d012b-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="d012b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d012b-146">-ResourceGroupName</span></span>
<span data-ttu-id="d012b-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d012b-147">The name of the resource group.</span></span>
<span data-ttu-id="d012b-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d012b-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d012b-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d012b-149">-SubscriptionId</span></span>
<span data-ttu-id="d012b-150">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d012b-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d012b-151">-Version</span><span class="sxs-lookup"><span data-stu-id="d012b-151">-Version</span></span>
<span data-ttu-id="d012b-152">Package Version found in the appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="d012b-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d012b-153">-Confirm</span></span>
<span data-ttu-id="d012b-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d012b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d012b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d012b-155">-WhatIf</span></span>
<span data-ttu-id="d012b-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d012b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d012b-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d012b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d012b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d012b-158">CommonParameters</span></span>
<span data-ttu-id="d012b-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d012b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d012b-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d012b-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d012b-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d012b-161">INPUTS</span></span>

## <span data-ttu-id="d012b-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d012b-162">OUTPUTS</span></span>

### <span data-ttu-id="d012b-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d012b-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="d012b-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d012b-164">NOTES</span></span>

<span data-ttu-id="d012b-165">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d012b-165">ALIASES</span></span>

<span data-ttu-id="d012b-166">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d012b-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d012b-167">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d012b-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d012b-168">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d012b-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d012b-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: Csomagalkalmazások listája.</span><span class="sxs-lookup"><span data-stu-id="d012b-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="d012b-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="d012b-171">`[AppUserModelId <String>]`: A Package Application aktiválásához használható.</span><span class="sxs-lookup"><span data-stu-id="d012b-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="d012b-172">Csomagnévből és ApplicationID-ből áll.</span><span class="sxs-lookup"><span data-stu-id="d012b-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="d012b-173">Található appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="d012b-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="d012b-174">`[Description <String>]`: A csomagalkalmazás leírása.</span><span class="sxs-lookup"><span data-stu-id="d012b-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="d012b-175">`[FriendlyName <String>]`: Felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="d012b-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="d012b-176">`[IconImageName <String>]`: Felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="d012b-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="d012b-177">`[RawIcon <Byte[]>]`: az ikon egy 64 bites karakterlánc bájttömbként.</span><span class="sxs-lookup"><span data-stu-id="d012b-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="d012b-178">`[RawPng <Byte[]>]`: az ikon egy 64 bites karakterlánc bájttömbként.</span><span class="sxs-lookup"><span data-stu-id="d012b-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="d012b-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: Csomagfüggések listája.</span><span class="sxs-lookup"><span data-stu-id="d012b-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="d012b-180">`[DependencyName <String>]`: A csomagfüggőség neve.</span><span class="sxs-lookup"><span data-stu-id="d012b-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="d012b-181">`[MinVersion <String>]`: A függőségi verzió szükséges.</span><span class="sxs-lookup"><span data-stu-id="d012b-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="d012b-182">`[Publisher <String>]`: A függőségi közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="d012b-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="d012b-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d012b-183">RELATED LINKS</span></span>

