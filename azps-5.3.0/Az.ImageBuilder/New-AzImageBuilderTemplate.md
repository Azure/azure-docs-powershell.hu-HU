---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386790"
---
# <span data-ttu-id="6cafc-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="6cafc-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="6cafc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cafc-102">SYNOPSIS</span></span>
<span data-ttu-id="6cafc-103">Virtuális gép képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="6cafc-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="6cafc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cafc-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cafc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cafc-105">DESCRIPTION</span></span>
<span data-ttu-id="6cafc-106">Virtuális gép képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="6cafc-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="6cafc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cafc-107">EXAMPLES</span></span>

### <span data-ttu-id="6cafc-108">1. példa: Virtuális gép képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="6cafc-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="6cafc-109">Ez a parancs virtuális gép képsablont hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6cafc-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="6cafc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cafc-110">PARAMETERS</span></span>

### <span data-ttu-id="6cafc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cafc-111">-AsJob</span></span>
<span data-ttu-id="6cafc-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6cafc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6cafc-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="6cafc-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="6cafc-114">A képsablon létrehozása közben várakozási idő maximális hossza.</span><span class="sxs-lookup"><span data-stu-id="6cafc-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="6cafc-115">Az alapértelmezett érték (4 óra) megadásához ne adjon meg 0-t.</span><span class="sxs-lookup"><span data-stu-id="6cafc-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="6cafc-116">-Testreszabás</span><span class="sxs-lookup"><span data-stu-id="6cafc-116">-Customize</span></span>
<span data-ttu-id="6cafc-117">Megadja a kép testreszabási lépéseit leíró tulajdonságokat, például a képforrást stb. A tulajdonságok testreszabása és a kivonattábla létrehozása a JEGYZETEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="6cafc-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cafc-118">-DefaultProfile</span></span>
<span data-ttu-id="6cafc-119">régió HideParameter Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cafc-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cafc-120">-Distribute</span><span class="sxs-lookup"><span data-stu-id="6cafc-120">-Distribute</span></span>
<span data-ttu-id="6cafc-121">Az eloszlás azt a célt tűzi ki, ahová a képkimenetnek át kell mennie.</span><span class="sxs-lookup"><span data-stu-id="6cafc-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="6cafc-122">A FELépítésről a NOTES (JEGYZETEK) szakaszban láthatja a DISTRIBUTE tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="6cafc-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="6cafc-123">-ImageTemplateName</span></span>
<span data-ttu-id="6cafc-124">A képsablon neve.</span><span class="sxs-lookup"><span data-stu-id="6cafc-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="6cafc-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="6cafc-126">Az utolsó futtatás záró időpontja (UTC).</span><span class="sxs-lookup"><span data-stu-id="6cafc-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="6cafc-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="6cafc-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="6cafc-128">Részletes információk a legutóbbi futtatás állapotáról.</span><span class="sxs-lookup"><span data-stu-id="6cafc-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="6cafc-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="6cafc-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="6cafc-130">Az utolsó futtatás állapota.</span><span class="sxs-lookup"><span data-stu-id="6cafc-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="6cafc-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="6cafc-132">Az utolsó futtatás alállapota.</span><span class="sxs-lookup"><span data-stu-id="6cafc-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="6cafc-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="6cafc-134">Az utolsó futtatás kezdési időpontja (UTC).</span><span class="sxs-lookup"><span data-stu-id="6cafc-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="6cafc-135">-Location</span><span class="sxs-lookup"><span data-stu-id="6cafc-135">-Location</span></span>
<span data-ttu-id="6cafc-136">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6cafc-136">Resource location.</span></span>

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

### <span data-ttu-id="6cafc-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6cafc-137">-NoWait</span></span>
<span data-ttu-id="6cafc-138">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6cafc-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cafc-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="6cafc-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="6cafc-140">A kiépítési hiba hibakódja.</span><span class="sxs-lookup"><span data-stu-id="6cafc-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="6cafc-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="6cafc-142">Részletes hibaüzenet a kiépítési hibáról.</span><span class="sxs-lookup"><span data-stu-id="6cafc-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="6cafc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cafc-143">-ResourceGroupName</span></span>
<span data-ttu-id="6cafc-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cafc-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cafc-145">-Source</span><span class="sxs-lookup"><span data-stu-id="6cafc-145">-Source</span></span>
<span data-ttu-id="6cafc-146">Virtuális gépi képforrást ismertet, amely a virtuális gép képforrását ismerteti az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="6cafc-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="6cafc-147">A forrástulajdonságok létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="6cafc-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafc-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cafc-148">-SubscriptionId</span></span>
<span data-ttu-id="6cafc-149">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6cafc-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="6cafc-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="6cafc-150">-Tag</span></span>
<span data-ttu-id="6cafc-151">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="6cafc-151">Resource tags.</span></span>

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

### <span data-ttu-id="6cafc-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="6cafc-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="6cafc-153">A felhasználóhoz rendelt identitás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cafc-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="6cafc-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="6cafc-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="6cafc-155">Az operációs rendszer lemezének mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="6cafc-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="6cafc-156">Az Azure alapértelmezett operációsrendszer-lemezméretének beállításhoz adja meg a 0 értéket, vagy adja meg a 0 értéket.</span><span class="sxs-lookup"><span data-stu-id="6cafc-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="6cafc-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="6cafc-157">-VMProfileVmSize</span></span>
<span data-ttu-id="6cafc-158">A képek felépítéséhez, testreszabásához és rögzítéséhez használt virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="6cafc-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="6cafc-159">Az alapértelmezett (Standard_D1_v2) megadásához kihagyja vagy megadja az üres Standard_D1_v2.</span><span class="sxs-lookup"><span data-stu-id="6cafc-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="6cafc-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="6cafc-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="6cafc-161">Egy meglévő alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cafc-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="6cafc-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cafc-162">-Confirm</span></span>
<span data-ttu-id="6cafc-163">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cafc-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cafc-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cafc-164">-WhatIf</span></span>
<span data-ttu-id="6cafc-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cafc-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cafc-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cafc-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cafc-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cafc-167">CommonParameters</span></span>
<span data-ttu-id="6cafc-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cafc-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cafc-169">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cafc-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cafc-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cafc-170">INPUTS</span></span>

## <span data-ttu-id="6cafc-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cafc-171">OUTPUTS</span></span>

### <span data-ttu-id="6cafc-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="6cafc-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="6cafc-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cafc-173">NOTES</span></span>

<span data-ttu-id="6cafc-174">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cafc-174">ALIASES</span></span>

<span data-ttu-id="6cafc-175">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6cafc-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cafc-176">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6cafc-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cafc-177">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cafc-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cafc-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Megadja a kép testreszabási lépéseit leíró tulajdonságokat, például a képforrást stb.</span><span class="sxs-lookup"><span data-stu-id="6cafc-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="6cafc-179">`Type <String>`: A képen használni kívánt testreszabási eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="6cafc-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="6cafc-180">A "Shell" lehet például shell customizer</span><span class="sxs-lookup"><span data-stu-id="6cafc-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="6cafc-181">`[Name <String>]`: Rövid név, amely kontextust nyújt arról, hogy mit tesz ez a testreszabási lépés</span><span class="sxs-lookup"><span data-stu-id="6cafc-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="6cafc-182">DISTRIBUTE <IImageTemplateDistributor[]>: Az a terjesztési cél, ahová a képkimenetnek át kell mennie.</span><span class="sxs-lookup"><span data-stu-id="6cafc-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="6cafc-183">`RunOutputName <String>`: A társított RunOutput-hoz használt név.</span><span class="sxs-lookup"><span data-stu-id="6cafc-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="6cafc-184">`Type <String>`: Az eloszlás típusa.</span><span class="sxs-lookup"><span data-stu-id="6cafc-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="6cafc-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Az összetevőre a terjesztő által létrehozott/frissített címkék.</span><span class="sxs-lookup"><span data-stu-id="6cafc-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="6cafc-186">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="6cafc-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="6cafc-187">FORRÁS: Egy virtuális gép <IImageTemplateSource> képforrását ismerteti, építés, testreszabás és terjesztés számára.</span><span class="sxs-lookup"><span data-stu-id="6cafc-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="6cafc-188">`Type <String>`: Azt adja meg, hogy milyen típusú forrásképpel szeretne kezdeni.</span><span class="sxs-lookup"><span data-stu-id="6cafc-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="6cafc-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cafc-189">RELATED LINKS</span></span>

