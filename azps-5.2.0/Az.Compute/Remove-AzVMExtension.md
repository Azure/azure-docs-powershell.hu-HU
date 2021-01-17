---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355422"
---
# <span data-ttu-id="5b837-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b837-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="5b837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b837-102">SYNOPSIS</span></span>
<span data-ttu-id="5b837-103">Eltávolít egy bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5b837-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="5b837-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b837-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b837-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b837-105">DESCRIPTION</span></span>
<span data-ttu-id="5b837-106">A **Remove-AzVMExtension** parancsmag eltávolít egy bővítményt a virtuális gép virtuális gép bővítményeiből.</span><span class="sxs-lookup"><span data-stu-id="5b837-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="5b837-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b837-107">EXAMPLES</span></span>

### <span data-ttu-id="5b837-108">1. példa: Bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="5b837-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="5b837-109">Ez a parancs eltávolítja a ContosoTest kiterjesztést a VirtualMachine22 nevű virtuális gépről az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="5b837-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="5b837-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b837-110">PARAMETERS</span></span>

### <span data-ttu-id="5b837-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b837-111">-DefaultProfile</span></span>
<span data-ttu-id="5b837-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b837-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b837-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5b837-113">-Force</span></span>
<span data-ttu-id="5b837-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b837-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b837-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5b837-115">-Name</span></span>
<span data-ttu-id="5b837-116">Annak a kiterjesztésnek a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5b837-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b837-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b837-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b837-118">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b837-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b837-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b837-119">-VMName</span></span>
<span data-ttu-id="5b837-120">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5b837-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="5b837-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b837-121">-Confirm</span></span>
<span data-ttu-id="5b837-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b837-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b837-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b837-123">-WhatIf</span></span>
<span data-ttu-id="5b837-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b837-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b837-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b837-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b837-126">CommonParameters</span></span>
<span data-ttu-id="5b837-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b837-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b837-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b837-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b837-129">INPUTS</span></span>

### <span data-ttu-id="5b837-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b837-130">System.String</span></span>

## <span data-ttu-id="5b837-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b837-131">OUTPUTS</span></span>

### <span data-ttu-id="5b837-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5b837-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5b837-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b837-133">NOTES</span></span>

## <span data-ttu-id="5b837-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b837-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b837-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b837-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="5b837-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b837-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


