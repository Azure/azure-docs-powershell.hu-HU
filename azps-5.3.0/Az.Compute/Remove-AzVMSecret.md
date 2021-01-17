---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480751"
---
# <span data-ttu-id="b1398-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="b1398-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="b1398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1398-102">SYNOPSIS</span></span>
<span data-ttu-id="b1398-103">Eltávolít (a) titkos(a)t egy virtuális gépi objektumból</span><span class="sxs-lookup"><span data-stu-id="b1398-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="b1398-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1398-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1398-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1398-105">DESCRIPTION</span></span>
<span data-ttu-id="b1398-106">A Remove-AzVMSecret parancsmag eltávolítja a (a) titkos(a)t egy virtuális gépi objektumból.</span><span class="sxs-lookup"><span data-stu-id="b1398-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="b1398-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1398-107">EXAMPLES</span></span>

### <span data-ttu-id="b1398-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b1398-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="b1398-109">Eltávolítja a virtuális gép "vm1" minden titka az "rg1" erőforráscsoportban, és frissíti a VM-et</span><span class="sxs-lookup"><span data-stu-id="b1398-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="b1398-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1398-110">PARAMETERS</span></span>

### <span data-ttu-id="b1398-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1398-111">-DefaultProfile</span></span>
<span data-ttu-id="b1398-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1398-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1398-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b1398-113">-SourceVaultId</span></span>
<span data-ttu-id="b1398-114">A parancsmag által eltávolítandó forrástár-kiosztások tömbje.</span><span class="sxs-lookup"><span data-stu-id="b1398-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1398-115">-VM</span><span class="sxs-lookup"><span data-stu-id="b1398-115">-VM</span></span>
<span data-ttu-id="b1398-116">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja az (a) titkos(a) titkos(a)t.</span><span class="sxs-lookup"><span data-stu-id="b1398-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="b1398-117">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b1398-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="b1398-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1398-118">-Confirm</span></span>
<span data-ttu-id="b1398-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b1398-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1398-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1398-120">-WhatIf</span></span>
<span data-ttu-id="b1398-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b1398-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1398-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1398-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1398-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1398-123">CommonParameters</span></span>
<span data-ttu-id="b1398-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1398-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1398-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1398-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1398-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1398-126">INPUTS</span></span>

### <span data-ttu-id="b1398-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1398-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1398-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1398-128">OUTPUTS</span></span>

### <span data-ttu-id="b1398-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1398-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1398-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1398-130">NOTES</span></span>

## <span data-ttu-id="b1398-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1398-131">RELATED LINKS</span></span>
