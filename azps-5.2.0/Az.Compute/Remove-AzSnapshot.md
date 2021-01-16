---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366070"
---
# <span data-ttu-id="156ec-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="156ec-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="156ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156ec-102">SYNOPSIS</span></span>
<span data-ttu-id="156ec-103">Egy pillanatfelvétel eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="156ec-103">Removes a snapshot.</span></span>

## <span data-ttu-id="156ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="156ec-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="156ec-105">DESCRIPTION</span></span>
<span data-ttu-id="156ec-106">A **Remove-AzSnapshot** parancsmag eltávolítja a pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="156ec-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="156ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="156ec-107">EXAMPLES</span></span>

### <span data-ttu-id="156ec-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="156ec-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="156ec-109">Ez a parancs eltávolítja a "Snapshot01" pillanatképet az "ResourceGroup01" erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="156ec-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="156ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="156ec-110">PARAMETERS</span></span>

### <span data-ttu-id="156ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="156ec-111">-AsJob</span></span>
<span data-ttu-id="156ec-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="156ec-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="156ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156ec-113">-DefaultProfile</span></span>
<span data-ttu-id="156ec-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="156ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="156ec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="156ec-115">-Force</span></span>
<span data-ttu-id="156ec-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="156ec-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="156ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="156ec-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="156ec-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="156ec-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="156ec-119">-SnapshotName</span></span>
<span data-ttu-id="156ec-120">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="156ec-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="156ec-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="156ec-121">-Confirm</span></span>
<span data-ttu-id="156ec-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="156ec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156ec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156ec-123">-WhatIf</span></span>
<span data-ttu-id="156ec-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="156ec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156ec-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="156ec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ec-126">CommonParameters</span></span>
<span data-ttu-id="156ec-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ec-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="156ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ec-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="156ec-129">INPUTS</span></span>

### <span data-ttu-id="156ec-130">System.String</span><span class="sxs-lookup"><span data-stu-id="156ec-130">System.String</span></span>

## <span data-ttu-id="156ec-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="156ec-131">OUTPUTS</span></span>

### <span data-ttu-id="156ec-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="156ec-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="156ec-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="156ec-133">NOTES</span></span>

## <span data-ttu-id="156ec-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="156ec-134">RELATED LINKS</span></span>
