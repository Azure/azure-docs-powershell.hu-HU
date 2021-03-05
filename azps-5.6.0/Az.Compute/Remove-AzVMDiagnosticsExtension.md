---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5b5a27be50da8a9c05b0cf766d48efe5844a0452
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009205"
---
# <span data-ttu-id="3fa8b-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa8b-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3fa8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa8b-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="3fa8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3fa8b-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa8b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3fa8b-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa8b-106">A **Remove-AzVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3fa8b-107">A módosítások megvalósításához át kell adni a parancsmag kimenetét Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3fa8b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3fa8b-108">EXAMPLES</span></span>

### <span data-ttu-id="3fa8b-109">1. példa: A diagnosztikai bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="3fa8b-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="3fa8b-110">Ez a parancs eltávolítja a Diagnosztikai bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3fa8b-111">A parancs a folyamat műveleti Update-AzVM parancsmagnak továbbküldi az eredményt.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3fa8b-112">Ez a parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3fa8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fa8b-113">PARAMETERS</span></span>

### <span data-ttu-id="3fa8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa8b-114">-DefaultProfile</span></span>
<span data-ttu-id="3fa8b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa8b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3fa8b-116">-Name</span></span>
<span data-ttu-id="3fa8b-117">A parancsmag által eltávolított Diagnosztikai bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8b-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3fa8b-118">-NoWait</span></span>
<span data-ttu-id="3fa8b-119">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3fa8b-120">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3fa8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fa8b-122">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3fa8b-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3fa8b-123">-VMName</span></span>
<span data-ttu-id="3fa8b-124">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolít egy diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="3fa8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa8b-125">CommonParameters</span></span>
<span data-ttu-id="3fa8b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa8b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fa8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa8b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fa8b-128">INPUTS</span></span>

### <span data-ttu-id="3fa8b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3fa8b-129">System.String</span></span>

## <span data-ttu-id="3fa8b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fa8b-130">OUTPUTS</span></span>

### <span data-ttu-id="3fa8b-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3fa8b-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3fa8b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3fa8b-132">NOTES</span></span>

## <span data-ttu-id="3fa8b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fa8b-133">RELATED LINKS</span></span>

[<span data-ttu-id="3fa8b-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa8b-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3fa8b-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa8b-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3fa8b-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3fa8b-136">Update-AzVM</span></span>](./Update-AzVM.md)


