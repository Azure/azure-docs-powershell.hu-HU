---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 30b3ee76a538b4db69e79397bff65e723a9bf908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007061"
---
# <span data-ttu-id="6079f-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6079f-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="6079f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6079f-102">SYNOPSIS</span></span>
<span data-ttu-id="6079f-103">Eltávolít egy DSC bővítménykezelőt egy erőforráscsoport virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="6079f-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6079f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6079f-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6079f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6079f-105">DESCRIPTION</span></span>
<span data-ttu-id="6079f-106">A **Remove-AzVMDscExtension** parancsmag eltávolítja a kívánt államkonfigurációs bővítménykezelőt egy erőforráscsoport virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="6079f-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6079f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6079f-107">EXAMPLES</span></span>

### <span data-ttu-id="6079f-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6079f-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="6079f-109">Ez a parancs eltávolítja a DSC nevű bővítményt a VM07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6079f-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="6079f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6079f-110">PARAMETERS</span></span>

### <span data-ttu-id="6079f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6079f-111">-DefaultProfile</span></span>
<span data-ttu-id="6079f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6079f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6079f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6079f-113">-Name</span></span>
<span data-ttu-id="6079f-114">A parancsmag által eltávolított DSC-bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="6079f-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="6079f-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft.Powershell.DSC értékre állítja, amely a **Remove-AzVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="6079f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6079f-116">-NoWait</span></span>
<span data-ttu-id="6079f-117">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="6079f-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6079f-118">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="6079f-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6079f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6079f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6079f-120">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6079f-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6079f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6079f-121">-VMName</span></span>
<span data-ttu-id="6079f-122">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja a DSC kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="6079f-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6079f-123">-Confirm</span></span>
<span data-ttu-id="6079f-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6079f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6079f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6079f-125">-WhatIf</span></span>
<span data-ttu-id="6079f-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6079f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6079f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6079f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6079f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6079f-128">CommonParameters</span></span>
<span data-ttu-id="6079f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6079f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6079f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6079f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6079f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6079f-131">INPUTS</span></span>

### <span data-ttu-id="6079f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6079f-132">System.String</span></span>

## <span data-ttu-id="6079f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6079f-133">OUTPUTS</span></span>

### <span data-ttu-id="6079f-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6079f-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6079f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6079f-135">NOTES</span></span>

## <span data-ttu-id="6079f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6079f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6079f-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6079f-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="6079f-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6079f-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


