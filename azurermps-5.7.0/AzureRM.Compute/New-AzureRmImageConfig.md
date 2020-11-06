---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503843"
---
# <span data-ttu-id="9ff40-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="9ff40-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="9ff40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ff40-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff40-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9ff40-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ff40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ff40-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ff40-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff40-106">A **New-AzureRmImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="9ff40-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="9ff40-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ff40-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff40-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ff40-108">Example 1</span></span>
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

<span data-ttu-id="9ff40-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9ff40-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="9ff40-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="9ff40-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="9ff40-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="9ff40-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="9ff40-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="9ff40-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="9ff40-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="9ff40-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="9ff40-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="9ff40-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9ff40-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ff40-115">PARAMETERS</span></span>

### <span data-ttu-id="9ff40-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="9ff40-116">-DataDisk</span></span>
<span data-ttu-id="9ff40-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff40-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="9ff40-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="9ff40-118">-Location</span></span>
<span data-ttu-id="9ff40-119">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="9ff40-119">Specifies a location.</span></span>

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

### <span data-ttu-id="9ff40-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="9ff40-120">-OsDisk</span></span>
<span data-ttu-id="9ff40-121">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff40-121">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="9ff40-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="9ff40-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="9ff40-123">A forrás virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff40-123">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="9ff40-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="9ff40-124">-Tag</span></span>
<span data-ttu-id="9ff40-125">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="9ff40-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="9ff40-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ff40-126">-Confirm</span></span>
<span data-ttu-id="9ff40-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ff40-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff40-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff40-128">-WhatIf</span></span>
<span data-ttu-id="9ff40-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ff40-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ff40-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ff40-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff40-131">CommonParameters</span></span>
<span data-ttu-id="9ff40-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ff40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff40-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff40-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff40-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ff40-134">INPUTS</span></span>

### <span data-ttu-id="9ff40-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff40-135">System.String</span></span>
<span data-ttu-id="9ff40-136">System. Collections. Hashtable. ImageOSDisk. microsoft. Azure. Management. kiszámítás. models. microsoft. Azure. Management. kiszámítás. models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="9ff40-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="9ff40-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ff40-137">OUTPUTS</span></span>

### <span data-ttu-id="9ff40-138">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="9ff40-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="9ff40-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ff40-139">NOTES</span></span>

## <span data-ttu-id="9ff40-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ff40-140">RELATED LINKS</span></span>

