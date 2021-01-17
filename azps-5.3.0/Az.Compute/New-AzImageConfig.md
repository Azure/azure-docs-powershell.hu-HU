---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477726"
---
# <span data-ttu-id="3bc43-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="3bc43-101">New-AzImageConfig</span></span>

## <span data-ttu-id="3bc43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc43-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc43-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3bc43-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="3bc43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bc43-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc43-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bc43-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc43-106">A **New-AzImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="3bc43-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="3bc43-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bc43-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc43-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3bc43-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="3bc43-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="3bc43-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3bc43-110">A következő három parancs az operációs rendszer lemezének elérési útját és két adatlemezt rendel a $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3bc43-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="3bc43-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát közelíti meg.</span><span class="sxs-lookup"><span data-stu-id="3bc43-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3bc43-112">A következő három parancs egy operációs rendszerlemezt és két adatlemezt ad hozzá a $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3bc43-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3bc43-113">Az egyes lemezeket a $osDiskVhdUri, a $dataDiskVhdUri 1 és a $dataDiskVhdUri 2 tárolja.</span><span class="sxs-lookup"><span data-stu-id="3bc43-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3bc43-114">Az utolsó parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3bc43-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3bc43-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bc43-115">PARAMETERS</span></span>

### <span data-ttu-id="3bc43-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="3bc43-116">-DataDisk</span></span>
<span data-ttu-id="3bc43-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bc43-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc43-118">-DefaultProfile</span></span>
<span data-ttu-id="3bc43-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bc43-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-120">-HyperVGeneráció</span><span class="sxs-lookup"><span data-stu-id="3bc43-120">-HyperVGeneration</span></span>
<span data-ttu-id="3bc43-121">A képből létrehozott virtuális gép HiperVGeneráció típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bc43-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="3bc43-122">Az engedélyezett értékek a V1 és a V2.</span><span class="sxs-lookup"><span data-stu-id="3bc43-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-123">-Location</span><span class="sxs-lookup"><span data-stu-id="3bc43-123">-Location</span></span>
<span data-ttu-id="3bc43-124">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="3bc43-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="3bc43-125">-OsDisk</span></span>
<span data-ttu-id="3bc43-126">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bc43-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3bc43-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="3bc43-128">A forrás virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3bc43-128">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bc43-129">-Tag</span></span>
<span data-ttu-id="3bc43-130">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="3bc43-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3bc43-131">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="3bc43-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc43-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="3bc43-132">-ZoneResilient</span></span>
<span data-ttu-id="3bc43-133">A zóna ellenállóvá tételének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="3bc43-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="3bc43-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bc43-134">-Confirm</span></span>
<span data-ttu-id="3bc43-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3bc43-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc43-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc43-136">-WhatIf</span></span>
<span data-ttu-id="3bc43-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3bc43-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bc43-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bc43-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc43-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc43-139">CommonParameters</span></span>
<span data-ttu-id="3bc43-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc43-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc43-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bc43-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc43-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bc43-142">INPUTS</span></span>

### <span data-ttu-id="3bc43-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3bc43-143">System.String</span></span>

### <span data-ttu-id="3bc43-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3bc43-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3bc43-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="3bc43-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="3bc43-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="3bc43-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="3bc43-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc43-147">OUTPUTS</span></span>

### <span data-ttu-id="3bc43-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="3bc43-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3bc43-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bc43-149">NOTES</span></span>

## <span data-ttu-id="3bc43-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bc43-150">RELATED LINKS</span></span>
