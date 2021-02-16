---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144771"
---
# <span data-ttu-id="b7673-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b7673-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="b7673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7673-102">SYNOPSIS</span></span>
<span data-ttu-id="b7673-103">Eltávolít egy bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="b7673-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="b7673-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7673-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7673-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7673-105">DESCRIPTION</span></span>
<span data-ttu-id="b7673-106">A **Remove-AzVMExtension** parancsmag eltávolít egy bővítményt a virtuális gép virtuális gép bővítményeiből.</span><span class="sxs-lookup"><span data-stu-id="b7673-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="b7673-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7673-107">EXAMPLES</span></span>

### <span data-ttu-id="b7673-108">1. példa: Bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="b7673-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="b7673-109">Ez a parancs eltávolítja a ContosoTest kiterjesztést a VirtualMachine22 nevű virtuális gépről az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="b7673-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="b7673-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7673-110">PARAMETERS</span></span>

### <span data-ttu-id="b7673-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7673-111">-DefaultProfile</span></span>
<span data-ttu-id="b7673-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7673-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7673-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b7673-113">-Force</span></span>
<span data-ttu-id="b7673-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b7673-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7673-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7673-115">-Name</span></span>
<span data-ttu-id="b7673-116">Annak a kiterjesztésnek a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b7673-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7673-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7673-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7673-118">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7673-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b7673-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b7673-119">-VMName</span></span>
<span data-ttu-id="b7673-120">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="b7673-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7673-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7673-121">-Confirm</span></span>
<span data-ttu-id="b7673-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7673-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7673-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7673-123">-WhatIf</span></span>
<span data-ttu-id="b7673-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7673-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7673-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7673-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7673-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7673-126">CommonParameters</span></span>
<span data-ttu-id="b7673-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7673-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7673-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7673-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7673-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7673-129">INPUTS</span></span>

### <span data-ttu-id="b7673-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b7673-130">System.String</span></span>

## <span data-ttu-id="b7673-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7673-131">OUTPUTS</span></span>

### <span data-ttu-id="b7673-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b7673-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b7673-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7673-133">NOTES</span></span>

## <span data-ttu-id="b7673-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7673-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7673-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b7673-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="b7673-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b7673-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


