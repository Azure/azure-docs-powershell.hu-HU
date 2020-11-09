---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296267"
---
# <span data-ttu-id="8b9d3-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="8b9d3-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="8b9d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9d3-103">Ez a cikk ismerteti a virtuális gép képforrását az épület, a Testreszabás és a terjesztés céljából.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="8b9d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b9d3-104">SYNTAX</span></span>

### <span data-ttu-id="8b9d3-105">ManagedImage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b9d3-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="8b9d3-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="8b9d3-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="8b9d3-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="8b9d3-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9d3-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b9d3-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8b9d3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b9d3-109">DESCRIPTION</span></span>
<span data-ttu-id="8b9d3-110">Ez a cikk ismerteti a virtuális gép képforrását az épület, a Testreszabás és a terjesztés céljából.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="8b9d3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8b9d3-111">EXAMPLES</span></span>

### <span data-ttu-id="8b9d3-112">Példa 1: felügyelt képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="8b9d3-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="8b9d3-113">Ezzel a paranccsal létrehozhatja a felügyelt képforrást.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="8b9d3-114">2. példa: megosztott képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="8b9d3-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="8b9d3-115">A parancs létrehoz egy megosztott képforrást.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="8b9d3-116">3. példa: platfrom-képes forrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="8b9d3-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="8b9d3-117">Ez a parancs létrehoz egy platfrom-képforrást.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="8b9d3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b9d3-118">PARAMETERS</span></span>

### <span data-ttu-id="8b9d3-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="8b9d3-119">-ImageId</span></span>
<span data-ttu-id="8b9d3-120">A felügyelt kép ARM erőforrás-azonosítója az ügyfél-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="8b9d3-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="8b9d3-121">-ImageVersionId</span></span>
<span data-ttu-id="8b9d3-122">A megosztott képgyűjteményben lévő kép verziószáma az ARM erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="8b9d3-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="8b9d3-123">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="8b9d3-123">-Offer</span></span>
<span data-ttu-id="8b9d3-124">Képajánlat az [Azure Gallery képei](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)közül.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="8b9d3-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8b9d3-125">-PlanName</span></span>
<span data-ttu-id="8b9d3-126">A beszerzési terv neve.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="8b9d3-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="8b9d3-127">-PlanProduct</span></span>
<span data-ttu-id="8b9d3-128">A vételi terv szorzata.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="8b9d3-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8b9d3-129">-PlanPublisher</span></span>
<span data-ttu-id="8b9d3-130">A vásárlási terv közzétevője</span><span class="sxs-lookup"><span data-stu-id="8b9d3-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="8b9d3-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8b9d3-131">-Publisher</span></span>
<span data-ttu-id="8b9d3-132">Image Publisher az [Azure Gallery képeiben](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="8b9d3-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="8b9d3-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b9d3-133">-Sku</span></span>
<span data-ttu-id="8b9d3-134">Image SKU az [Azure Gallery-képekből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="8b9d3-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="8b9d3-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="8b9d3-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="8b9d3-136">Ez a cikk az előfizetésben szereplő, felügyelt képeket tartalmazó képforrást ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="8b9d3-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="8b9d3-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="8b9d3-138">Az [Azure Gallery képekből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)származó képforrást ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="8b9d3-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b9d3-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="8b9d3-140">A cikkben egy képforrást ismertet, amely a megosztott képgyűjteményben lévő képfájl.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="8b9d3-141">-Verzió</span><span class="sxs-lookup"><span data-stu-id="8b9d3-141">-Version</span></span>
<span data-ttu-id="8b9d3-142">Kép verziója az [Azure Gallery képeiből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="8b9d3-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="8b9d3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9d3-143">CommonParameters</span></span>
<span data-ttu-id="8b9d3-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b9d3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9d3-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b9d3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9d3-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b9d3-146">INPUTS</span></span>

## <span data-ttu-id="8b9d3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b9d3-147">OUTPUTS</span></span>

### <span data-ttu-id="8b9d3-148">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="8b9d3-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="8b9d3-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b9d3-149">NOTES</span></span>

<span data-ttu-id="8b9d3-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8b9d3-150">ALIASES</span></span>

## <span data-ttu-id="8b9d3-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b9d3-151">RELATED LINKS</span></span>

