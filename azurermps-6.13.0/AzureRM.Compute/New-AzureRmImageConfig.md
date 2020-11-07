---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: f2d5903de64655b79765774f7232790f8a00ffc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680395"
---
# <span data-ttu-id="29b29-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="29b29-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="29b29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29b29-102">SYNOPSIS</span></span>
<span data-ttu-id="29b29-103">Konfigurálható képobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29b29-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29b29-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29b29-105">DESCRIPTION</span></span>
<span data-ttu-id="29b29-106">A **New-AzureRmImageConfig** parancsmag létrehoz egy konfigurálható képobjektumot.</span><span class="sxs-lookup"><span data-stu-id="29b29-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="29b29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29b29-107">EXAMPLES</span></span>

### <span data-ttu-id="29b29-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29b29-108">Example 1</span></span>
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

<span data-ttu-id="29b29-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29b29-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="29b29-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="29b29-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="29b29-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="29b29-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="29b29-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="29b29-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="29b29-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="29b29-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="29b29-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="29b29-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="29b29-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29b29-115">PARAMETERS</span></span>

### <span data-ttu-id="29b29-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="29b29-116">-DataDisk</span></span>
<span data-ttu-id="29b29-117">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b29-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="29b29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b29-118">-DefaultProfile</span></span>
<span data-ttu-id="29b29-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29b29-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b29-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="29b29-120">-Location</span></span>
<span data-ttu-id="29b29-121">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="29b29-121">Specifies a location.</span></span>

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

### <span data-ttu-id="29b29-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="29b29-122">-OsDisk</span></span>
<span data-ttu-id="29b29-123">Az operációs rendszer lemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b29-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="29b29-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="29b29-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="29b29-125">A forrás virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b29-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="29b29-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="29b29-126">-Tag</span></span>
<span data-ttu-id="29b29-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="29b29-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="29b29-128">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="29b29-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="29b29-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="29b29-129">-ZoneResilient</span></span>
<span data-ttu-id="29b29-130">A zóna rugalmas engedélyezése</span><span class="sxs-lookup"><span data-stu-id="29b29-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="29b29-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29b29-131">-Confirm</span></span>
<span data-ttu-id="29b29-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29b29-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b29-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b29-133">-WhatIf</span></span>
<span data-ttu-id="29b29-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29b29-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29b29-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29b29-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b29-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b29-136">CommonParameters</span></span>
<span data-ttu-id="29b29-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29b29-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b29-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b29-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b29-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b29-139">INPUTS</span></span>

### <span data-ttu-id="29b29-140">System. String</span><span class="sxs-lookup"><span data-stu-id="29b29-140">System.String</span></span>

### <span data-ttu-id="29b29-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="29b29-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="29b29-142">Microsoft. Azure. Management. kiszámítás. models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="29b29-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="29b29-143">Microsoft. Azure. Management. számítás. models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="29b29-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="29b29-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b29-144">OUTPUTS</span></span>

### <span data-ttu-id="29b29-145">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="29b29-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="29b29-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29b29-146">NOTES</span></span>

## <span data-ttu-id="29b29-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29b29-147">RELATED LINKS</span></span>
