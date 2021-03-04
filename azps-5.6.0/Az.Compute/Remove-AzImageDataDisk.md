---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934265"
---
# <span data-ttu-id="a67ff-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="a67ff-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="a67ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a67ff-103">Eltávolít egy adatlemezt egy képobjektumból.</span><span class="sxs-lookup"><span data-stu-id="a67ff-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="a67ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a67ff-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67ff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a67ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a67ff-106">A **Remove-AzImageDataDisk** parancsmag eltávolít egy adatlemezt egy képobjektumból.</span><span class="sxs-lookup"><span data-stu-id="a67ff-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="a67ff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a67ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a67ff-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a67ff-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="a67ff-109">Ez a parancs eltávolítja az 1. logikai egység adatlemezét az "ResourceGroup01" erőforráscsoport meglévő "Image01" képén.</span><span class="sxs-lookup"><span data-stu-id="a67ff-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a67ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a67ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67ff-111">-DefaultProfile</span></span>
<span data-ttu-id="a67ff-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a67ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a67ff-113">-Image</span><span class="sxs-lookup"><span data-stu-id="a67ff-113">-Image</span></span>
<span data-ttu-id="a67ff-114">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a67ff-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ff-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="a67ff-115">-Lun</span></span>
<span data-ttu-id="a67ff-116">A logikai egység számát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="a67ff-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ff-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a67ff-117">-Confirm</span></span>
<span data-ttu-id="a67ff-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a67ff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67ff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67ff-119">-WhatIf</span></span>
<span data-ttu-id="a67ff-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a67ff-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a67ff-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a67ff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67ff-122">CommonParameters</span></span>
<span data-ttu-id="a67ff-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67ff-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a67ff-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67ff-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a67ff-125">INPUTS</span></span>

### <span data-ttu-id="a67ff-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="a67ff-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="a67ff-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a67ff-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a67ff-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a67ff-128">OUTPUTS</span></span>

### <span data-ttu-id="a67ff-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="a67ff-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a67ff-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a67ff-130">NOTES</span></span>

## <span data-ttu-id="a67ff-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a67ff-131">RELATED LINKS</span></span>
