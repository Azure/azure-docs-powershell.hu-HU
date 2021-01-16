---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363746"
---
# <span data-ttu-id="06da6-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06da6-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="06da6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06da6-102">SYNOPSIS</span></span>
<span data-ttu-id="06da6-103">Eltávolít egy DSC bővítménykezelőt egy erőforráscsoport virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="06da6-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="06da6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06da6-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06da6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06da6-105">DESCRIPTION</span></span>
<span data-ttu-id="06da6-106">A **Remove-AzVMDscExtension** parancsmag eltávolítja a kívánt államkonfigurációs bővítménykezelőt egy erőforráscsoport virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="06da6-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="06da6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06da6-107">EXAMPLES</span></span>

### <span data-ttu-id="06da6-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="06da6-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="06da6-109">Ez a parancs eltávolítja a DSC nevű bővítményt a VM07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="06da6-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="06da6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06da6-110">PARAMETERS</span></span>

### <span data-ttu-id="06da6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06da6-111">-DefaultProfile</span></span>
<span data-ttu-id="06da6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06da6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06da6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="06da6-113">-Name</span></span>
<span data-ttu-id="06da6-114">A parancsmag által eltávolított DSC-bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="06da6-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="06da6-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft.Powershell.DSC értékre állítja, amely a **Remove-AzVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="06da6-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="06da6-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06da6-116">-NoWait</span></span>
<span data-ttu-id="06da6-117">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="06da6-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="06da6-118">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="06da6-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="06da6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06da6-119">-ResourceGroupName</span></span>
<span data-ttu-id="06da6-120">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="06da6-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="06da6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="06da6-121">-VMName</span></span>
<span data-ttu-id="06da6-122">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja a DSC kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="06da6-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="06da6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06da6-123">-Confirm</span></span>
<span data-ttu-id="06da6-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06da6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06da6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06da6-125">-WhatIf</span></span>
<span data-ttu-id="06da6-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06da6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06da6-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06da6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06da6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06da6-128">CommonParameters</span></span>
<span data-ttu-id="06da6-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06da6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06da6-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06da6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06da6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06da6-131">INPUTS</span></span>

### <span data-ttu-id="06da6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="06da6-132">System.String</span></span>

## <span data-ttu-id="06da6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06da6-133">OUTPUTS</span></span>

### <span data-ttu-id="06da6-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="06da6-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="06da6-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06da6-135">NOTES</span></span>

## <span data-ttu-id="06da6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06da6-136">RELATED LINKS</span></span>

[<span data-ttu-id="06da6-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06da6-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="06da6-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="06da6-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


