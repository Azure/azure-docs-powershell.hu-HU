---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347513"
---
# <span data-ttu-id="06122-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="06122-101">Remove-AzDisk</span></span>

## <span data-ttu-id="06122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06122-102">SYNOPSIS</span></span>
<span data-ttu-id="06122-103">Lemez eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="06122-103">Removes a disk.</span></span>

## <span data-ttu-id="06122-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06122-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06122-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06122-105">DESCRIPTION</span></span>
<span data-ttu-id="06122-106">Az **Remove-AzDisk** parancsmag eltávolítja a lemezeket.</span><span class="sxs-lookup"><span data-stu-id="06122-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="06122-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06122-107">EXAMPLES</span></span>

### <span data-ttu-id="06122-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="06122-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="06122-109">Ez a parancs eltávolítja a "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="06122-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="06122-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06122-110">PARAMETERS</span></span>

### <span data-ttu-id="06122-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06122-111">-AsJob</span></span>
<span data-ttu-id="06122-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="06122-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="06122-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06122-113">-DefaultProfile</span></span>
<span data-ttu-id="06122-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06122-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06122-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="06122-115">-DiskName</span></span>
<span data-ttu-id="06122-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06122-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="06122-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06122-117">-Force</span></span>
<span data-ttu-id="06122-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="06122-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06122-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06122-119">-ResourceGroupName</span></span>
<span data-ttu-id="06122-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06122-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="06122-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06122-121">-Confirm</span></span>
<span data-ttu-id="06122-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06122-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06122-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06122-123">-WhatIf</span></span>
<span data-ttu-id="06122-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06122-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06122-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06122-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06122-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06122-126">CommonParameters</span></span>
<span data-ttu-id="06122-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06122-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06122-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06122-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06122-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06122-129">INPUTS</span></span>

### <span data-ttu-id="06122-130">System.String</span><span class="sxs-lookup"><span data-stu-id="06122-130">System.String</span></span>

## <span data-ttu-id="06122-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06122-131">OUTPUTS</span></span>

### <span data-ttu-id="06122-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="06122-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="06122-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06122-133">NOTES</span></span>

## <span data-ttu-id="06122-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06122-134">RELATED LINKS</span></span>
