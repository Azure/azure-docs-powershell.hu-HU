---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 892a3f6f47bd24046777aabd648fb2702d09961b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836752"
---
# <span data-ttu-id="d56b2-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="d56b2-101">New-AzImage</span></span>

## <span data-ttu-id="d56b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d56b2-102">SYNOPSIS</span></span>
<span data-ttu-id="d56b2-103">Képet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d56b2-103">Creates an image.</span></span>

## <span data-ttu-id="d56b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d56b2-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d56b2-105">DESCRIPTION</span></span>
<span data-ttu-id="d56b2-106">A **New-AzImage** parancsmag létrehoz egy képet.</span><span class="sxs-lookup"><span data-stu-id="d56b2-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="d56b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d56b2-107">EXAMPLES</span></span>

### <span data-ttu-id="d56b2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d56b2-108">Example 1</span></span>
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

<span data-ttu-id="d56b2-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d56b2-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="d56b2-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="d56b2-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d56b2-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="d56b2-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="d56b2-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="d56b2-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d56b2-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d56b2-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="d56b2-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="d56b2-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d56b2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d56b2-115">PARAMETERS</span></span>

### <span data-ttu-id="d56b2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d56b2-116">-AsJob</span></span>
<span data-ttu-id="d56b2-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d56b2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d56b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56b2-118">-DefaultProfile</span></span>
<span data-ttu-id="d56b2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d56b2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56b2-120">-Kép</span><span class="sxs-lookup"><span data-stu-id="d56b2-120">-Image</span></span>
<span data-ttu-id="d56b2-121">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d56b2-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56b2-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d56b2-122">-ImageName</span></span>
<span data-ttu-id="d56b2-123">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d56b2-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d56b2-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d56b2-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56b2-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d56b2-126">-Confirm</span></span>
<span data-ttu-id="d56b2-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d56b2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56b2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56b2-128">-WhatIf</span></span>
<span data-ttu-id="d56b2-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d56b2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56b2-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d56b2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56b2-131">CommonParameters</span></span>
<span data-ttu-id="d56b2-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d56b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56b2-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56b2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56b2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d56b2-134">INPUTS</span></span>

### <span data-ttu-id="d56b2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d56b2-135">System.String</span></span>

### <span data-ttu-id="d56b2-136">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d56b2-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d56b2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d56b2-137">OUTPUTS</span></span>

### <span data-ttu-id="d56b2-138">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d56b2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d56b2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d56b2-139">NOTES</span></span>

## <span data-ttu-id="d56b2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d56b2-140">RELATED LINKS</span></span>
