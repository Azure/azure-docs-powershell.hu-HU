---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018114"
---
# <span data-ttu-id="a2d00-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2d00-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a2d00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2d00-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d00-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a2d00-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="a2d00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2d00-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d00-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2d00-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d00-106">A **Remove-AzVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a2d00-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="a2d00-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a2d00-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="a2d00-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a2d00-108">EXAMPLES</span></span>

### <span data-ttu-id="a2d00-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="a2d00-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="a2d00-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a2d00-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="a2d00-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a2d00-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a2d00-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a2d00-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="a2d00-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2d00-113">PARAMETERS</span></span>

### <span data-ttu-id="a2d00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d00-114">-DefaultProfile</span></span>
<span data-ttu-id="a2d00-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2d00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d00-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2d00-116">-Name</span></span>
<span data-ttu-id="a2d00-117">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="a2d00-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a2d00-118">-Várva</span><span class="sxs-lookup"><span data-stu-id="a2d00-118">-NoWait</span></span>
<span data-ttu-id="a2d00-119">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="a2d00-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a2d00-120">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a2d00-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a2d00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d00-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2d00-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2d00-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a2d00-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2d00-123">-VMName</span></span>
<span data-ttu-id="a2d00-124">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a2d00-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="a2d00-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d00-125">CommonParameters</span></span>
<span data-ttu-id="a2d00-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2d00-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d00-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2d00-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d00-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2d00-128">INPUTS</span></span>

### <span data-ttu-id="a2d00-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d00-129">System.String</span></span>

## <span data-ttu-id="a2d00-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2d00-130">OUTPUTS</span></span>

### <span data-ttu-id="a2d00-131">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a2d00-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a2d00-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2d00-132">NOTES</span></span>

## <span data-ttu-id="a2d00-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2d00-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2d00-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2d00-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a2d00-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2d00-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a2d00-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a2d00-136">Update-AzVM</span></span>](./Update-AzVM.md)


