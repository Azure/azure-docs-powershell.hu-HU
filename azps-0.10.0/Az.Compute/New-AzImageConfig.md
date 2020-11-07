---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de6c09c6c86fa4da7eff57439f556d21d18d94a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844490"
---
# <span data-ttu-id="c7437-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="c7437-101">New-AzImageConfig</span></span>

## <span data-ttu-id="c7437-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7437-102">SYNOPSIS</span></span>
<span data-ttu-id="c7437-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c7437-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="c7437-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7437-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7437-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7437-105">DESCRIPTION</span></span>
<span data-ttu-id="c7437-106">A **New-AzImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="c7437-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="c7437-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7437-107">EXAMPLES</span></span>

### <span data-ttu-id="c7437-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7437-108">Example 1</span></span>
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

<span data-ttu-id="c7437-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c7437-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="c7437-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="c7437-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="c7437-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="c7437-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="c7437-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="c7437-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c7437-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c7437-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="c7437-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="c7437-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c7437-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7437-115">PARAMETERS</span></span>

### <span data-ttu-id="c7437-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="c7437-116">-DataDisk</span></span>
<span data-ttu-id="c7437-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7437-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7437-118">-DefaultProfile</span></span>
<span data-ttu-id="c7437-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7437-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="c7437-120">-Location</span></span>
<span data-ttu-id="c7437-121">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c7437-121">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="c7437-122">-OsDisk</span></span>
<span data-ttu-id="c7437-123">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7437-123">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c7437-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="c7437-125">A forrás virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7437-125">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="c7437-126">-Tag</span></span>
<span data-ttu-id="c7437-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="c7437-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7437-128">Példa:</span><span class="sxs-lookup"><span data-stu-id="c7437-128">For example:</span></span>

<span data-ttu-id="c7437-129">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c7437-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7437-130">-Confirm</span></span>
<span data-ttu-id="c7437-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7437-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7437-132">-WhatIf</span></span>
<span data-ttu-id="c7437-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7437-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7437-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7437-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7437-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7437-135">CommonParameters</span></span>
<span data-ttu-id="c7437-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7437-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7437-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7437-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7437-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7437-138">INPUTS</span></span>

### <span data-ttu-id="c7437-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7437-139">None</span></span>
<span data-ttu-id="c7437-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c7437-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7437-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7437-141">OUTPUTS</span></span>

### <span data-ttu-id="c7437-142">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c7437-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c7437-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7437-143">NOTES</span></span>

## <span data-ttu-id="c7437-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7437-144">RELATED LINKS</span></span>

