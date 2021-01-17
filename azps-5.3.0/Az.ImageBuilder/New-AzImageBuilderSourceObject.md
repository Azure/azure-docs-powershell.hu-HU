---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466029"
---
# <span data-ttu-id="fd482-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="fd482-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="fd482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd482-102">SYNOPSIS</span></span>
<span data-ttu-id="fd482-103">Virtuális gépi képforrást ismertet, amely a virtuális gép képforrását ismerteti az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="fd482-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="fd482-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd482-104">SYNTAX</span></span>

### <span data-ttu-id="fd482-105">ManagedImage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd482-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="fd482-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="fd482-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="fd482-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="fd482-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd482-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="fd482-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="fd482-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd482-109">DESCRIPTION</span></span>
<span data-ttu-id="fd482-110">Virtuális gépi képforrást ismertet, amely a virtuális gép képforrását ismerteti az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="fd482-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="fd482-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd482-111">EXAMPLES</span></span>

### <span data-ttu-id="fd482-112">1. példa: Felügyelt képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd482-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="fd482-113">Ez a parancs egy felügyelt képforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd482-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="fd482-114">2. példa: Megosztott képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd482-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="fd482-115">Ez a parancs megosztott képforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd482-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="fd482-116">3. példa: Platfrom képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd482-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="fd482-117">Ez a parancs egy képforrásból származó platfromot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd482-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="fd482-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd482-118">PARAMETERS</span></span>

### <span data-ttu-id="fd482-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="fd482-119">-ImageId</span></span>
<span data-ttu-id="fd482-120">ARM ügyfél-előfizetésben a felügyelt kép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd482-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="fd482-121">-ImageVersionId</span></span>
<span data-ttu-id="fd482-122">ARM kép verziójának erőforrás-azonosítója a megosztott képgyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="fd482-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="fd482-123">-Offer</span></span>
<span data-ttu-id="fd482-124">Képajánlat az [Azure Galéria képtárából.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="fd482-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="fd482-125">-PlanName</span></span>
<span data-ttu-id="fd482-126">A vásárlási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="fd482-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="fd482-127">-PlanProduct</span></span>
<span data-ttu-id="fd482-128">A vásárlási csomag terméke.</span><span class="sxs-lookup"><span data-stu-id="fd482-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fd482-129">-PlanPublisher</span></span>
<span data-ttu-id="fd482-130">A vásárlási csomag kiadója.</span><span class="sxs-lookup"><span data-stu-id="fd482-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fd482-131">-Publisher</span></span>
<span data-ttu-id="fd482-132">Képkiadó az [Azure Galéria képtárában.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="fd482-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="fd482-133">-Sku</span></span>
<span data-ttu-id="fd482-134">Képváltozat az [Azure Galéria képeiből.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="fd482-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="fd482-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="fd482-136">Ez a témakör az ügyfél-előfizetés felügyelt képének képforrását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="fd482-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="fd482-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="fd482-138">Ez a cikk az Azure Gallery Images [szolgáltatásból származó képforrást ismerteti.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="fd482-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="fd482-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="fd482-140">Olyan képforrást ismertet, amely egy képverzió egy megosztott képgyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="fd482-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-141">-Version</span><span class="sxs-lookup"><span data-stu-id="fd482-141">-Version</span></span>
<span data-ttu-id="fd482-142">Kép verziója az [Azure Galéria képtárából.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="fd482-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd482-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd482-143">CommonParameters</span></span>
<span data-ttu-id="fd482-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd482-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd482-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd482-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd482-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd482-146">INPUTS</span></span>

## <span data-ttu-id="fd482-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd482-147">OUTPUTS</span></span>

### <span data-ttu-id="fd482-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="fd482-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="fd482-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd482-149">NOTES</span></span>

<span data-ttu-id="fd482-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fd482-150">ALIASES</span></span>

## <span data-ttu-id="fd482-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd482-151">RELATED LINKS</span></span>

