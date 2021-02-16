---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204887"
---
# <span data-ttu-id="53f7c-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="53f7c-101">New-AzImage</span></span>

## <span data-ttu-id="53f7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="53f7c-103">Létrehoz egy képet.</span><span class="sxs-lookup"><span data-stu-id="53f7c-103">Creates an image.</span></span>

## <span data-ttu-id="53f7c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53f7c-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f7c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53f7c-105">DESCRIPTION</span></span>
<span data-ttu-id="53f7c-106">A **New-AzImage parancsmag** létrehoz egy képet.</span><span class="sxs-lookup"><span data-stu-id="53f7c-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="53f7c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53f7c-107">EXAMPLES</span></span>

### <span data-ttu-id="53f7c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="53f7c-108">Example 1</span></span>
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

<span data-ttu-id="53f7c-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="53f7c-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="53f7c-110">A következő három parancs az operációs rendszer lemezének elérési útját és két adatlemezt rendel a $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="53f7c-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="53f7c-111">Ez a módszer csak az alábbi parancsok olvashatóságát közelíti meg.</span><span class="sxs-lookup"><span data-stu-id="53f7c-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="53f7c-112">A következő három parancs egy operációs rendszerlemezt és két adatlemezt ad hozzá a $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="53f7c-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="53f7c-113">Az egyes lemezeket a $osDiskVhdUri, a $dataDiskVhdUri 1 és a $dataDiskVhdUri 2 tárolja.</span><span class="sxs-lookup"><span data-stu-id="53f7c-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="53f7c-114">Az utolsó parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="53f7c-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="53f7c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53f7c-115">PARAMETERS</span></span>

### <span data-ttu-id="53f7c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f7c-116">-AsJob</span></span>
<span data-ttu-id="53f7c-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53f7c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53f7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f7c-118">-DefaultProfile</span></span>
<span data-ttu-id="53f7c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53f7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f7c-120">-Image</span><span class="sxs-lookup"><span data-stu-id="53f7c-120">-Image</span></span>
<span data-ttu-id="53f7c-121">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="53f7c-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="53f7c-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="53f7c-122">-ImageName</span></span>
<span data-ttu-id="53f7c-123">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53f7c-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="53f7c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f7c-124">-ResourceGroupName</span></span>
<span data-ttu-id="53f7c-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53f7c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53f7c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53f7c-126">-Confirm</span></span>
<span data-ttu-id="53f7c-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53f7c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f7c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f7c-128">-WhatIf</span></span>
<span data-ttu-id="53f7c-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53f7c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f7c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53f7c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f7c-131">CommonParameters</span></span>
<span data-ttu-id="53f7c-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f7c-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53f7c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f7c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53f7c-134">INPUTS</span></span>

### <span data-ttu-id="53f7c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="53f7c-135">System.String</span></span>

### <span data-ttu-id="53f7c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="53f7c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="53f7c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53f7c-137">OUTPUTS</span></span>

### <span data-ttu-id="53f7c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="53f7c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="53f7c-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53f7c-139">NOTES</span></span>

## <span data-ttu-id="53f7c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53f7c-140">RELATED LINKS</span></span>
