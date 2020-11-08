---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011458"
---
# <span data-ttu-id="b983a-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="b983a-101">New-AzImage</span></span>

## <span data-ttu-id="b983a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b983a-102">SYNOPSIS</span></span>
<span data-ttu-id="b983a-103">Képet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b983a-103">Creates an image.</span></span>

## <span data-ttu-id="b983a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b983a-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b983a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b983a-105">DESCRIPTION</span></span>
<span data-ttu-id="b983a-106">A **New-AzImage** parancsmag létrehoz egy képet.</span><span class="sxs-lookup"><span data-stu-id="b983a-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="b983a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b983a-107">EXAMPLES</span></span>

### <span data-ttu-id="b983a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b983a-108">Example 1</span></span>
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

<span data-ttu-id="b983a-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b983a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="b983a-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="b983a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="b983a-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="b983a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b983a-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="b983a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="b983a-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="b983a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="b983a-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="b983a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b983a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b983a-115">PARAMETERS</span></span>

### <span data-ttu-id="b983a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b983a-116">-AsJob</span></span>
<span data-ttu-id="b983a-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b983a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b983a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b983a-118">-DefaultProfile</span></span>
<span data-ttu-id="b983a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b983a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b983a-120">-Kép</span><span class="sxs-lookup"><span data-stu-id="b983a-120">-Image</span></span>
<span data-ttu-id="b983a-121">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b983a-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="b983a-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b983a-122">-ImageName</span></span>
<span data-ttu-id="b983a-123">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b983a-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b983a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b983a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b983a-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b983a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b983a-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b983a-126">-Confirm</span></span>
<span data-ttu-id="b983a-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b983a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b983a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b983a-128">-WhatIf</span></span>
<span data-ttu-id="b983a-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b983a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b983a-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b983a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b983a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b983a-131">CommonParameters</span></span>
<span data-ttu-id="b983a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b983a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b983a-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b983a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b983a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b983a-134">INPUTS</span></span>

### <span data-ttu-id="b983a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b983a-135">System.String</span></span>

### <span data-ttu-id="b983a-136">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b983a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b983a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b983a-137">OUTPUTS</span></span>

### <span data-ttu-id="b983a-138">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b983a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b983a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b983a-139">NOTES</span></span>

## <span data-ttu-id="b983a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b983a-140">RELATED LINKS</span></span>
