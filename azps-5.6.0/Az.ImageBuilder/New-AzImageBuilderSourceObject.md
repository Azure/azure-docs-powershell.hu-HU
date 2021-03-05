---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013045"
---
# <span data-ttu-id="b1538-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="b1538-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="b1538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1538-102">SYNOPSIS</span></span>
<span data-ttu-id="b1538-103">Virtuális gépi képforrást ismertet, amely a virtuális gép képforrását ismerteti az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="b1538-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="b1538-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1538-104">SYNTAX</span></span>

### <span data-ttu-id="b1538-105">ManagedImage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1538-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1538-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="b1538-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1538-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="b1538-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1538-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="b1538-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1538-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1538-109">DESCRIPTION</span></span>
<span data-ttu-id="b1538-110">Virtuális gépi képforrást ismertet, amely a virtuális gép képforrását ismerteti az építéshez, a testreszabáshoz és a terjesztéshez.</span><span class="sxs-lookup"><span data-stu-id="b1538-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="b1538-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1538-111">EXAMPLES</span></span>

### <span data-ttu-id="b1538-112">1. példa: Felügyelt képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b1538-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="b1538-113">Ez a parancs egy felügyelt képforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1538-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="b1538-114">2. példa: Megosztott képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b1538-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="b1538-115">Ez a parancs megosztott képforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1538-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="b1538-116">3. példa: Platfrom képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b1538-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="b1538-117">Ez a parancs egy képforrásból származó platfromot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1538-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="b1538-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1538-118">PARAMETERS</span></span>

### <span data-ttu-id="b1538-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="b1538-119">-ImageId</span></span>
<span data-ttu-id="b1538-120">ARM ügyfél-előfizetésben a felügyelt kép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1538-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="b1538-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="b1538-121">-ImageVersionId</span></span>
<span data-ttu-id="b1538-122">ARM kép verziójának erőforrás-azonosítója a megosztott képgyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="b1538-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="b1538-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="b1538-123">-Offer</span></span>
<span data-ttu-id="b1538-124">Képajánlat az [Azure Galéria képtárából.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b1538-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b1538-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b1538-125">-PlanName</span></span>
<span data-ttu-id="b1538-126">A vásárlási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="b1538-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="b1538-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b1538-127">-PlanProduct</span></span>
<span data-ttu-id="b1538-128">A vásárlási csomag terméke.</span><span class="sxs-lookup"><span data-stu-id="b1538-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="b1538-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b1538-129">-PlanPublisher</span></span>
<span data-ttu-id="b1538-130">A vásárlási csomag kiadója.</span><span class="sxs-lookup"><span data-stu-id="b1538-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="b1538-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b1538-131">-Publisher</span></span>
<span data-ttu-id="b1538-132">Képkiadó az [Azure Galéria képtárában.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b1538-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b1538-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="b1538-133">-Sku</span></span>
<span data-ttu-id="b1538-134">Képváltozat az [Azure Galéria képeiből.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b1538-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b1538-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="b1538-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="b1538-136">Ez a témakör az ügyfél-előfizetés felügyelt képének képforrását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b1538-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="b1538-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="b1538-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="b1538-138">Ez a cikk az Azure Gallery Images [szolgáltatásból származó képforrást ismerteti.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b1538-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b1538-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="b1538-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="b1538-140">Olyan képforrást ismertet, amely egy képverzió egy megosztott képgyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="b1538-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="b1538-141">-Version</span><span class="sxs-lookup"><span data-stu-id="b1538-141">-Version</span></span>
<span data-ttu-id="b1538-142">Kép verziója az [Azure Galéria képtárából.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b1538-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b1538-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1538-143">CommonParameters</span></span>
<span data-ttu-id="b1538-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1538-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1538-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1538-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1538-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1538-146">INPUTS</span></span>

## <span data-ttu-id="b1538-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1538-147">OUTPUTS</span></span>

### <span data-ttu-id="b1538-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="b1538-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="b1538-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1538-149">NOTES</span></span>

<span data-ttu-id="b1538-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b1538-150">ALIASES</span></span>

## <span data-ttu-id="b1538-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1538-151">RELATED LINKS</span></span>

