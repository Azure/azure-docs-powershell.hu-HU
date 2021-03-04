---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937082"
---
# <span data-ttu-id="90497-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="90497-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="90497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90497-102">SYNOPSIS</span></span>
<span data-ttu-id="90497-103">Eltávolítja a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="90497-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="90497-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90497-104">SYNTAX</span></span>

### <span data-ttu-id="90497-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90497-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90497-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="90497-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90497-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="90497-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90497-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90497-108">DESCRIPTION</span></span>
<span data-ttu-id="90497-109">Eltávolítja a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="90497-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="90497-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90497-110">EXAMPLES</span></span>

### <span data-ttu-id="90497-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="90497-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="90497-112">Delete disk encryption set 'enc1' in 'rg1'</span><span class="sxs-lookup"><span data-stu-id="90497-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="90497-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90497-113">PARAMETERS</span></span>

### <span data-ttu-id="90497-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90497-114">-AsJob</span></span>
<span data-ttu-id="90497-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="90497-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90497-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90497-116">-DefaultProfile</span></span>
<span data-ttu-id="90497-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90497-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90497-118">-Force</span><span class="sxs-lookup"><span data-stu-id="90497-118">-Force</span></span>
<span data-ttu-id="90497-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="90497-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="90497-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90497-120">-InputObject</span></span>
<span data-ttu-id="90497-121">A lemeztitkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="90497-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90497-122">-Name</span><span class="sxs-lookup"><span data-stu-id="90497-122">-Name</span></span>
<span data-ttu-id="90497-123">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="90497-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90497-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90497-124">-ResourceGroupName</span></span>
<span data-ttu-id="90497-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90497-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90497-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90497-126">-ResourceId</span></span>
<span data-ttu-id="90497-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90497-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90497-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90497-128">-Confirm</span></span>
<span data-ttu-id="90497-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90497-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90497-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90497-130">-WhatIf</span></span>
<span data-ttu-id="90497-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90497-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90497-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90497-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90497-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90497-133">CommonParameters</span></span>
<span data-ttu-id="90497-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90497-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90497-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90497-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90497-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90497-136">INPUTS</span></span>

### <span data-ttu-id="90497-137">System.String</span><span class="sxs-lookup"><span data-stu-id="90497-137">System.String</span></span>

### <span data-ttu-id="90497-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="90497-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="90497-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90497-139">OUTPUTS</span></span>

### <span data-ttu-id="90497-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="90497-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="90497-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90497-141">NOTES</span></span>

## <span data-ttu-id="90497-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90497-142">RELATED LINKS</span></span>
