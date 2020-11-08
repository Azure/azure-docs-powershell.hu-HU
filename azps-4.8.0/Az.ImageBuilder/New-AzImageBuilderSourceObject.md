---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183371"
---
# <span data-ttu-id="04d6c-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="04d6c-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="04d6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="04d6c-103">Ez a cikk ismerteti a virtuális gép képforrását az épület, a Testreszabás és a terjesztés céljából.</span><span class="sxs-lookup"><span data-stu-id="04d6c-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="04d6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04d6c-104">SYNTAX</span></span>

### <span data-ttu-id="04d6c-105">ManagedImage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04d6c-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="04d6c-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="04d6c-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="04d6c-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="04d6c-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="04d6c-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="04d6c-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="04d6c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="04d6c-109">DESCRIPTION</span></span>
<span data-ttu-id="04d6c-110">Ez a cikk ismerteti a virtuális gép képforrását az épület, a Testreszabás és a terjesztés céljából.</span><span class="sxs-lookup"><span data-stu-id="04d6c-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="04d6c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="04d6c-111">EXAMPLES</span></span>

### <span data-ttu-id="04d6c-112">Példa 1: felügyelt képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="04d6c-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="04d6c-113">Ezzel a paranccsal létrehozhatja a felügyelt képforrást.</span><span class="sxs-lookup"><span data-stu-id="04d6c-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="04d6c-114">2. példa: megosztott képforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="04d6c-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="04d6c-115">A parancs létrehoz egy megosztott képforrást.</span><span class="sxs-lookup"><span data-stu-id="04d6c-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="04d6c-116">3. példa: platfrom-képes forrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="04d6c-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="04d6c-117">Ez a parancs létrehoz egy platfrom-képforrást.</span><span class="sxs-lookup"><span data-stu-id="04d6c-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="04d6c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04d6c-118">PARAMETERS</span></span>

### <span data-ttu-id="04d6c-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="04d6c-119">-ImageId</span></span>
<span data-ttu-id="04d6c-120">A felügyelt kép ARM erőforrás-azonosítója az ügyfél-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="04d6c-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="04d6c-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="04d6c-121">-ImageVersionId</span></span>
<span data-ttu-id="04d6c-122">A megosztott képgyűjteményben lévő kép verziószáma az ARM erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="04d6c-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="04d6c-123">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="04d6c-123">-Offer</span></span>
<span data-ttu-id="04d6c-124">Képajánlat az [Azure Gallery képei](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)közül.</span><span class="sxs-lookup"><span data-stu-id="04d6c-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="04d6c-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="04d6c-125">-PlanName</span></span>
<span data-ttu-id="04d6c-126">A beszerzési terv neve.</span><span class="sxs-lookup"><span data-stu-id="04d6c-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="04d6c-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="04d6c-127">-PlanProduct</span></span>
<span data-ttu-id="04d6c-128">A vételi terv szorzata.</span><span class="sxs-lookup"><span data-stu-id="04d6c-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="04d6c-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="04d6c-129">-PlanPublisher</span></span>
<span data-ttu-id="04d6c-130">A vásárlási terv közzétevője</span><span class="sxs-lookup"><span data-stu-id="04d6c-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="04d6c-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="04d6c-131">-Publisher</span></span>
<span data-ttu-id="04d6c-132">Image Publisher az [Azure Gallery képeiben](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="04d6c-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="04d6c-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="04d6c-133">-Sku</span></span>
<span data-ttu-id="04d6c-134">Image SKU az [Azure Gallery-képekből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="04d6c-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="04d6c-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="04d6c-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="04d6c-136">Ez a cikk az előfizetésben szereplő, felügyelt képeket tartalmazó képforrást ismerteti.</span><span class="sxs-lookup"><span data-stu-id="04d6c-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="04d6c-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="04d6c-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="04d6c-138">Az [Azure Gallery képekből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)származó képforrást ismerteti.</span><span class="sxs-lookup"><span data-stu-id="04d6c-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="04d6c-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="04d6c-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="04d6c-140">A cikkben egy képforrást ismertet, amely a megosztott képgyűjteményben lévő képfájl.</span><span class="sxs-lookup"><span data-stu-id="04d6c-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="04d6c-141">-Verzió</span><span class="sxs-lookup"><span data-stu-id="04d6c-141">-Version</span></span>
<span data-ttu-id="04d6c-142">Kép verziója az [Azure Gallery képeiből](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="04d6c-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="04d6c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d6c-143">CommonParameters</span></span>
<span data-ttu-id="04d6c-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04d6c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d6c-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04d6c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d6c-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d6c-146">INPUTS</span></span>

## <span data-ttu-id="04d6c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d6c-147">OUTPUTS</span></span>

### <span data-ttu-id="04d6c-148">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="04d6c-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="04d6c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04d6c-149">NOTES</span></span>

<span data-ttu-id="04d6c-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="04d6c-150">ALIASES</span></span>

## <span data-ttu-id="04d6c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04d6c-151">RELATED LINKS</span></span>

