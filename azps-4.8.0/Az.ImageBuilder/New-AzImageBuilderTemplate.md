---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181913"
---
# <span data-ttu-id="a5922-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="a5922-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="a5922-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5922-102">SYNOPSIS</span></span>
<span data-ttu-id="a5922-103">Virtuális gép képsablonjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5922-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="a5922-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5922-104">SYNTAX</span></span>

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

## <span data-ttu-id="a5922-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5922-105">DESCRIPTION</span></span>
<span data-ttu-id="a5922-106">Virtuális gép képsablonjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5922-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="a5922-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5922-107">EXAMPLES</span></span>

### <span data-ttu-id="a5922-108">Példa 1: virtuális gép Képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="a5922-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="a5922-109">Ezzel a paranccsal létrehozhatja a virtuális gép képsablonját.</span><span class="sxs-lookup"><span data-stu-id="a5922-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="a5922-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5922-110">PARAMETERS</span></span>

### <span data-ttu-id="a5922-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5922-111">-AsJob</span></span>
<span data-ttu-id="a5922-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="a5922-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a5922-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="a5922-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="a5922-114">A Képsablon létrehozásakor megvárni kívánt maximális időtartam</span><span class="sxs-lookup"><span data-stu-id="a5922-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="a5922-115">Az alapértelmezett (4 óra) beállításnál hagyja ki vagy adja meg a 0 értéket.</span><span class="sxs-lookup"><span data-stu-id="a5922-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="a5922-116">-Testreszabás</span><span class="sxs-lookup"><span data-stu-id="a5922-116">-Customize</span></span>
<span data-ttu-id="a5922-117">A kép testreszabási lépéseinek (például a képforrásnak stb.) leírására szolgáló tulajdonságokat adja meg. A kivitelezéshez lásd: megjegyzések szakasz a tulajdonságok TESTRESZABÁSához és a kivonatoló táblázat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a5922-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5922-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5922-118">-DefaultProfile</span></span>
<span data-ttu-id="a5922-119">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések HideParameter.</span><span class="sxs-lookup"><span data-stu-id="a5922-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5922-120">-Distribution (terjesztés)</span><span class="sxs-lookup"><span data-stu-id="a5922-120">-Distribute</span></span>
<span data-ttu-id="a5922-121">Azok a terjesztési célok, amelyekben a kép kimenetének el kell térnie.</span><span class="sxs-lookup"><span data-stu-id="a5922-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="a5922-122">A kivitelezéshez lásd: megjegyzések szakasz a tulajdonságok ELOSZTÁSához és a kivonatoló táblázat létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a5922-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5922-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="a5922-123">-ImageTemplateName</span></span>
<span data-ttu-id="a5922-124">A Képsablon neve.</span><span class="sxs-lookup"><span data-stu-id="a5922-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="a5922-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="a5922-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="a5922-126">Az utolsó futás befejezési időpontja (UTC)</span><span class="sxs-lookup"><span data-stu-id="a5922-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="a5922-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="a5922-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="a5922-128">Részletes információk az utolsó futtatási állapotról.</span><span class="sxs-lookup"><span data-stu-id="a5922-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="a5922-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="a5922-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="a5922-130">Az utolsó Futtatás állapota</span><span class="sxs-lookup"><span data-stu-id="a5922-130">State of the last run.</span></span>

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

### <span data-ttu-id="a5922-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="a5922-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="a5922-132">Az utolsó Futtatás alszintű állapota</span><span class="sxs-lookup"><span data-stu-id="a5922-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="a5922-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="a5922-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="a5922-134">Az utolsó Futtatás kezdési időpontja (UTC)</span><span class="sxs-lookup"><span data-stu-id="a5922-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="a5922-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5922-135">-Location</span></span>
<span data-ttu-id="a5922-136">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a5922-136">Resource location.</span></span>

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

### <span data-ttu-id="a5922-137">-Várva</span><span class="sxs-lookup"><span data-stu-id="a5922-137">-NoWait</span></span>
<span data-ttu-id="a5922-138">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="a5922-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5922-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="a5922-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="a5922-140">A kiépítési hiba kódja.</span><span class="sxs-lookup"><span data-stu-id="a5922-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="a5922-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="a5922-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="a5922-142">Részletes hibaüzenet a kiépítési hibáról.</span><span class="sxs-lookup"><span data-stu-id="a5922-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="a5922-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5922-143">-ResourceGroupName</span></span>
<span data-ttu-id="a5922-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5922-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5922-145">-Forrás</span><span class="sxs-lookup"><span data-stu-id="a5922-145">-Source</span></span>
<span data-ttu-id="a5922-146">Ez a cikk ismerteti a virtuális gép képforrását az épület, a Testreszabás és a terjesztés céljából.</span><span class="sxs-lookup"><span data-stu-id="a5922-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="a5922-147">A kivitelezéshez lásd: megjegyzések szakasz a forrás tulajdonságaihoz, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a5922-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5922-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5922-148">-SubscriptionId</span></span>
<span data-ttu-id="a5922-149">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a5922-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="a5922-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="a5922-150">-Tag</span></span>
<span data-ttu-id="a5922-151">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="a5922-151">Resource tags.</span></span>

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

### <span data-ttu-id="a5922-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a5922-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a5922-153">A felhasználó által kiosztott identitás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5922-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="a5922-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a5922-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="a5922-155">Az operációs rendszer merevlemezének mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="a5922-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="a5922-156">Az Azure alapértelmezett operációsrendszer-méretének használatához hagyja meg vagy adja meg a 0 értéket.</span><span class="sxs-lookup"><span data-stu-id="a5922-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="a5922-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="a5922-157">-VMProfileVmSize</span></span>
<span data-ttu-id="a5922-158">A képek létrehozásához, testreszabásához és rögzítéséhez használt virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="a5922-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="a5922-159">Hagyja üresen vagy adjon meg egy üres karakterláncot az alapértelmezett (Standard_D1_v2) használatához.</span><span class="sxs-lookup"><span data-stu-id="a5922-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="a5922-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="a5922-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="a5922-161">Egy korábban létező alhálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5922-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="a5922-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5922-162">-Confirm</span></span>
<span data-ttu-id="a5922-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5922-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5922-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5922-164">-WhatIf</span></span>
<span data-ttu-id="a5922-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5922-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5922-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5922-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5922-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5922-167">CommonParameters</span></span>
<span data-ttu-id="a5922-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5922-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5922-169">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5922-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5922-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5922-170">INPUTS</span></span>

## <span data-ttu-id="a5922-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5922-171">OUTPUTS</span></span>

### <span data-ttu-id="a5922-172">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="a5922-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="a5922-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5922-173">NOTES</span></span>

<span data-ttu-id="a5922-174">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a5922-174">ALIASES</span></span>

<span data-ttu-id="a5922-175">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a5922-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5922-176">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a5922-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5922-177">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a5922-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5922-178">TESTRE <IImageTemplateCustomizer [] >: Itt adhatja meg a kép testreszabási lépéseit (például a képforrást stb.) leíró tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a5922-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="a5922-179">`Type <String>`: A képre használni kívánt testreszabási eszköz típusa.</span><span class="sxs-lookup"><span data-stu-id="a5922-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="a5922-180">Például a "Shell" lehet Shell-testre szabva</span><span class="sxs-lookup"><span data-stu-id="a5922-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="a5922-181">`[Name <String>]`: Felhasználóbarát név a testreszabási lépésekről a környezet megadásához</span><span class="sxs-lookup"><span data-stu-id="a5922-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="a5922-182">DISTRIBUTion <IImageTemplateDistributor [] >: a terjesztési célok, amelyekben a kép kimenetének el kell jutnia.</span><span class="sxs-lookup"><span data-stu-id="a5922-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="a5922-183">`RunOutputName <String>`: A kapcsolódó RunOutput használandó név.</span><span class="sxs-lookup"><span data-stu-id="a5922-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="a5922-184">`Type <String>`: A terjesztési típus.</span><span class="sxs-lookup"><span data-stu-id="a5922-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="a5922-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: A címkét, amelyet a program a forgalmazó által létrehozott/frissített, a tárgyhoz fog alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="a5922-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="a5922-186">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="a5922-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="a5922-187">FORRÁS <IImageTemplateSource> : leírja a virtuális gép képforrását az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="a5922-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="a5922-188">`Type <String>`: Itt adhatja meg, hogy milyen típusú képet szeretne kezdeni.</span><span class="sxs-lookup"><span data-stu-id="a5922-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="a5922-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5922-189">RELATED LINKS</span></span>

