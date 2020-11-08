---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187062"
---
# <span data-ttu-id="c43ed-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="c43ed-101">New-AzImageConfig</span></span>

## <span data-ttu-id="c43ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c43ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c43ed-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c43ed-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="c43ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c43ed-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c43ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c43ed-106">A **New-AzImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="c43ed-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="c43ed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c43ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c43ed-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c43ed-108">Example 1</span></span>
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

<span data-ttu-id="c43ed-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c43ed-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c43ed-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="c43ed-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="c43ed-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="c43ed-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c43ed-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="c43ed-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c43ed-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c43ed-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c43ed-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="c43ed-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c43ed-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c43ed-115">PARAMETERS</span></span>

### <span data-ttu-id="c43ed-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="c43ed-116">-DataDisk</span></span>
<span data-ttu-id="c43ed-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43ed-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="c43ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43ed-118">-DefaultProfile</span></span>
<span data-ttu-id="c43ed-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c43ed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c43ed-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="c43ed-120">-HyperVGeneration</span></span>
<span data-ttu-id="c43ed-121">A képből létrehozott virtuális gép HyperVGeneration típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43ed-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="c43ed-122">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="c43ed-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="c43ed-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="c43ed-123">-Location</span></span>
<span data-ttu-id="c43ed-124">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c43ed-124">Specifies a location.</span></span>

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

### <span data-ttu-id="c43ed-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="c43ed-125">-OsDisk</span></span>
<span data-ttu-id="c43ed-126">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43ed-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="c43ed-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c43ed-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="c43ed-128">A forrás virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c43ed-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="c43ed-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="c43ed-129">-Tag</span></span>
<span data-ttu-id="c43ed-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="c43ed-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c43ed-131">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c43ed-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c43ed-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="c43ed-132">-ZoneResilient</span></span>
<span data-ttu-id="c43ed-133">A zóna rugalmas engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c43ed-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="c43ed-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c43ed-134">-Confirm</span></span>
<span data-ttu-id="c43ed-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c43ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43ed-136">-WhatIf</span></span>
<span data-ttu-id="c43ed-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c43ed-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c43ed-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c43ed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43ed-139">CommonParameters</span></span>
<span data-ttu-id="c43ed-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c43ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43ed-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c43ed-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43ed-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c43ed-142">INPUTS</span></span>

### <span data-ttu-id="c43ed-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c43ed-143">System.String</span></span>

### <span data-ttu-id="c43ed-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c43ed-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c43ed-145">Microsoft. Azure. Management. kiszámítás. models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="c43ed-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="c43ed-146">Microsoft. Azure. Management. számítás. models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="c43ed-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="c43ed-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c43ed-147">OUTPUTS</span></span>

### <span data-ttu-id="c43ed-148">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c43ed-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c43ed-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c43ed-149">NOTES</span></span>

## <span data-ttu-id="c43ed-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c43ed-150">RELATED LINKS</span></span>
