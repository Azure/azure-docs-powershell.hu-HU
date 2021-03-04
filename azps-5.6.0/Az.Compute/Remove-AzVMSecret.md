---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935298"
---
# <span data-ttu-id="1d923-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="1d923-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="1d923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d923-102">SYNOPSIS</span></span>
<span data-ttu-id="1d923-103">Eltávolít (a) titkos(a)t egy virtuális gépi objektumból</span><span class="sxs-lookup"><span data-stu-id="1d923-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="1d923-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d923-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d923-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d923-105">DESCRIPTION</span></span>
<span data-ttu-id="1d923-106">A Remove-AzVMSecret parancsmag eltávolítja a (a) titkos(a)t egy virtuális gépi objektumból.</span><span class="sxs-lookup"><span data-stu-id="1d923-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="1d923-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d923-107">EXAMPLES</span></span>

### <span data-ttu-id="1d923-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1d923-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="1d923-109">Eltávolítja a virtuális gép "vm1" minden titka az "rg1" erőforráscsoportban, és frissíti a VM-et</span><span class="sxs-lookup"><span data-stu-id="1d923-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="1d923-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d923-110">PARAMETERS</span></span>

### <span data-ttu-id="1d923-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d923-111">-DefaultProfile</span></span>
<span data-ttu-id="1d923-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d923-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d923-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1d923-113">-SourceVaultId</span></span>
<span data-ttu-id="1d923-114">A parancsmag által eltávolítandó forrástár-kiosztások tömbje.</span><span class="sxs-lookup"><span data-stu-id="1d923-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d923-115">-VM</span><span class="sxs-lookup"><span data-stu-id="1d923-115">-VM</span></span>
<span data-ttu-id="1d923-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja az (a) titkos(a) titkos(a)t.</span><span class="sxs-lookup"><span data-stu-id="1d923-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="1d923-117">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d923-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d923-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d923-118">-Confirm</span></span>
<span data-ttu-id="1d923-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d923-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d923-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d923-120">-WhatIf</span></span>
<span data-ttu-id="1d923-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d923-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d923-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d923-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d923-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d923-123">CommonParameters</span></span>
<span data-ttu-id="1d923-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d923-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d923-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d923-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d923-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d923-126">INPUTS</span></span>

### <span data-ttu-id="1d923-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1d923-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1d923-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d923-128">OUTPUTS</span></span>

### <span data-ttu-id="1d923-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1d923-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1d923-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d923-130">NOTES</span></span>

## <span data-ttu-id="1d923-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d923-131">RELATED LINKS</span></span>
