---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204862"
---
# <span data-ttu-id="25e0f-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="25e0f-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="25e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="25e0f-103">Eltávolítja a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="25e0f-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="25e0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25e0f-104">SYNTAX</span></span>

### <span data-ttu-id="25e0f-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25e0f-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e0f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="25e0f-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e0f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="25e0f-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e0f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25e0f-108">DESCRIPTION</span></span>
<span data-ttu-id="25e0f-109">Eltávolítja a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="25e0f-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="25e0f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25e0f-110">EXAMPLES</span></span>

### <span data-ttu-id="25e0f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25e0f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="25e0f-112">Delete disk encryption set 'enc1' in 'rg1'</span><span class="sxs-lookup"><span data-stu-id="25e0f-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="25e0f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e0f-113">PARAMETERS</span></span>

### <span data-ttu-id="25e0f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25e0f-114">-AsJob</span></span>
<span data-ttu-id="25e0f-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="25e0f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25e0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e0f-116">-DefaultProfile</span></span>
<span data-ttu-id="25e0f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25e0f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e0f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="25e0f-118">-Force</span></span>
<span data-ttu-id="25e0f-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="25e0f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25e0f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e0f-120">-InputObject</span></span>
<span data-ttu-id="25e0f-121">A lemeztitkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="25e0f-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="25e0f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25e0f-122">-Name</span></span>
<span data-ttu-id="25e0f-123">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="25e0f-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="25e0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="25e0f-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25e0f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25e0f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25e0f-126">-ResourceId</span></span>
<span data-ttu-id="25e0f-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25e0f-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="25e0f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e0f-128">-Confirm</span></span>
<span data-ttu-id="25e0f-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="25e0f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e0f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e0f-130">-WhatIf</span></span>
<span data-ttu-id="25e0f-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="25e0f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e0f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25e0f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e0f-133">CommonParameters</span></span>
<span data-ttu-id="25e0f-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e0f-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e0f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e0f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25e0f-136">INPUTS</span></span>

### <span data-ttu-id="25e0f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="25e0f-137">System.String</span></span>

### <span data-ttu-id="25e0f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="25e0f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="25e0f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25e0f-139">OUTPUTS</span></span>

### <span data-ttu-id="25e0f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="25e0f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="25e0f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25e0f-141">NOTES</span></span>

## <span data-ttu-id="25e0f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25e0f-142">RELATED LINKS</span></span>
