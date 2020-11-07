---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848521"
---
# <span data-ttu-id="369a7-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="369a7-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="369a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="369a7-102">SYNOPSIS</span></span>
<span data-ttu-id="369a7-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="369a7-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="369a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="369a7-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="369a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="369a7-105">DESCRIPTION</span></span>
<span data-ttu-id="369a7-106">A **New-AzureRmImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="369a7-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="369a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="369a7-107">EXAMPLES</span></span>

### <span data-ttu-id="369a7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="369a7-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="369a7-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="369a7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="369a7-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="369a7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="369a7-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="369a7-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="369a7-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="369a7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="369a7-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="369a7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="369a7-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="369a7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="369a7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="369a7-115">PARAMETERS</span></span>

### <span data-ttu-id="369a7-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="369a7-116">-DataDisk</span></span>
<span data-ttu-id="369a7-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="369a7-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="369a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369a7-118">-DefaultProfile</span></span>
<span data-ttu-id="369a7-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="369a7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="369a7-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="369a7-120">-Location</span></span>
<span data-ttu-id="369a7-121">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="369a7-121">Specifies a location.</span></span>

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

### <span data-ttu-id="369a7-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="369a7-122">-OsDisk</span></span>
<span data-ttu-id="369a7-123">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="369a7-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="369a7-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="369a7-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="369a7-125">A forrás virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="369a7-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="369a7-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="369a7-126">-Tag</span></span>
<span data-ttu-id="369a7-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="369a7-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="369a7-128">Példa:</span><span class="sxs-lookup"><span data-stu-id="369a7-128">For example:</span></span>

<span data-ttu-id="369a7-129">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="369a7-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="369a7-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="369a7-130">-Confirm</span></span>
<span data-ttu-id="369a7-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="369a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="369a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="369a7-132">-WhatIf</span></span>
<span data-ttu-id="369a7-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="369a7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="369a7-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="369a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="369a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369a7-135">CommonParameters</span></span>
<span data-ttu-id="369a7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="369a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369a7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369a7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="369a7-138">INPUTS</span></span>

### <span data-ttu-id="369a7-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="369a7-139">None</span></span>
<span data-ttu-id="369a7-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="369a7-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="369a7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="369a7-141">OUTPUTS</span></span>

### <span data-ttu-id="369a7-142">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="369a7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="369a7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="369a7-143">NOTES</span></span>

## <span data-ttu-id="369a7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="369a7-144">RELATED LINKS</span></span>

