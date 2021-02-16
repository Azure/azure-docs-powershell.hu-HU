---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144850"
---
# <span data-ttu-id="0bb1f-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="0bb1f-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="0bb1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb1f-103">Eltávolít egy adatlemezt egy képobjektumból.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="0bb1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bb1f-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb1f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb1f-106">A **Remove-AzImageDataDisk** parancsmag eltávolít egy adatlemezt egy képobjektumból.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="0bb1f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bb1f-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb1f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0bb1f-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="0bb1f-109">Ez a parancs eltávolítja az 1. logikai egység adatlemezét az "ResourceGroup01" erőforráscsoport meglévő "Image01" képe alapján.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0bb1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bb1f-110">PARAMETERS</span></span>

### <span data-ttu-id="0bb1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb1f-111">-DefaultProfile</span></span>
<span data-ttu-id="0bb1f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb1f-113">-Image</span><span class="sxs-lookup"><span data-stu-id="0bb1f-113">-Image</span></span>
<span data-ttu-id="0bb1f-114">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="0bb1f-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="0bb1f-115">-Lun</span></span>
<span data-ttu-id="0bb1f-116">A logikai egység számát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="0bb1f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bb1f-117">-Confirm</span></span>
<span data-ttu-id="0bb1f-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb1f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb1f-119">-WhatIf</span></span>
<span data-ttu-id="0bb1f-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bb1f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb1f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb1f-122">CommonParameters</span></span>
<span data-ttu-id="0bb1f-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb1f-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bb1f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb1f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bb1f-125">INPUTS</span></span>

### <span data-ttu-id="0bb1f-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="0bb1f-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="0bb1f-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0bb1f-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0bb1f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bb1f-128">OUTPUTS</span></span>

### <span data-ttu-id="0bb1f-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="0bb1f-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0bb1f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bb1f-130">NOTES</span></span>

## <span data-ttu-id="0bb1f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bb1f-131">RELATED LINKS</span></span>
