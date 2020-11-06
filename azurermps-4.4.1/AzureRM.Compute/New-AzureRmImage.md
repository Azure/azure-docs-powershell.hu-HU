---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 02255fd8fd4db5747c820755bfd46ee3251aab9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492555"
---
# <span data-ttu-id="0ba73-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="0ba73-101">New-AzureRmImage</span></span>

## <span data-ttu-id="0ba73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ba73-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba73-103">Képet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0ba73-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ba73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ba73-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ba73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ba73-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba73-106">A **New-AzureRmImage** parancsmag létrehoz egy képet.</span><span class="sxs-lookup"><span data-stu-id="0ba73-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="0ba73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ba73-107">EXAMPLES</span></span>

### <span data-ttu-id="0ba73-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ba73-108">Example 1</span></span>
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

<span data-ttu-id="0ba73-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ba73-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="0ba73-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="0ba73-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0ba73-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="0ba73-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="0ba73-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="0ba73-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0ba73-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0ba73-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="0ba73-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="0ba73-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0ba73-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ba73-115">PARAMETERS</span></span>

### <span data-ttu-id="0ba73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba73-116">-DefaultProfile</span></span>
<span data-ttu-id="0ba73-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ba73-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ba73-118">-Kép</span><span class="sxs-lookup"><span data-stu-id="0ba73-118">-Image</span></span>
<span data-ttu-id="0ba73-119">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ba73-119">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba73-120">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0ba73-120">-ImageName</span></span>
<span data-ttu-id="0ba73-121">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba73-121">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba73-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ba73-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ba73-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba73-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ba73-124">-Confirm</span></span>
<span data-ttu-id="0ba73-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ba73-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ba73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ba73-126">-WhatIf</span></span>
<span data-ttu-id="0ba73-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ba73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ba73-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ba73-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ba73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba73-129">CommonParameters</span></span>
<span data-ttu-id="0ba73-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ba73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba73-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba73-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba73-132">INPUTS</span></span>

### <span data-ttu-id="0ba73-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba73-133">System.String</span></span>
<span data-ttu-id="0ba73-134">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="0ba73-134">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="0ba73-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ba73-135">OUTPUTS</span></span>

### <span data-ttu-id="0ba73-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="0ba73-136">System.Object</span></span>

## <span data-ttu-id="0ba73-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ba73-137">NOTES</span></span>

## <span data-ttu-id="0ba73-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ba73-138">RELATED LINKS</span></span>

