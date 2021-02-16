---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166458"
---
# <span data-ttu-id="ef240-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="ef240-101">Remove-AzImage</span></span>

## <span data-ttu-id="ef240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef240-102">SYNOPSIS</span></span>
<span data-ttu-id="ef240-103">Eltávolít egy képet.</span><span class="sxs-lookup"><span data-stu-id="ef240-103">Removes an image.</span></span>

## <span data-ttu-id="ef240-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef240-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef240-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef240-105">DESCRIPTION</span></span>
<span data-ttu-id="ef240-106">Az **Remove-AzImage parancsmag** eltávolítja a képet.</span><span class="sxs-lookup"><span data-stu-id="ef240-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="ef240-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef240-107">EXAMPLES</span></span>

### <span data-ttu-id="ef240-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef240-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="ef240-109">Ez a parancs eltávolítja az "Image01" nevű képet az "ResourceGroup01" erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="ef240-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ef240-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef240-110">PARAMETERS</span></span>

### <span data-ttu-id="ef240-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef240-111">-AsJob</span></span>
<span data-ttu-id="ef240-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ef240-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ef240-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef240-113">-DefaultProfile</span></span>
<span data-ttu-id="ef240-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef240-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef240-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef240-115">-Force</span></span>
<span data-ttu-id="ef240-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ef240-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef240-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ef240-117">-ImageName</span></span>
<span data-ttu-id="ef240-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef240-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ef240-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef240-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef240-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef240-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ef240-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef240-121">-Confirm</span></span>
<span data-ttu-id="ef240-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef240-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef240-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef240-123">-WhatIf</span></span>
<span data-ttu-id="ef240-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef240-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef240-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef240-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef240-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef240-126">CommonParameters</span></span>
<span data-ttu-id="ef240-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef240-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef240-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef240-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef240-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef240-129">INPUTS</span></span>

### <span data-ttu-id="ef240-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ef240-130">System.String</span></span>

## <span data-ttu-id="ef240-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef240-131">OUTPUTS</span></span>

### <span data-ttu-id="ef240-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ef240-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ef240-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef240-133">NOTES</span></span>

## <span data-ttu-id="ef240-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef240-134">RELATED LINKS</span></span>
