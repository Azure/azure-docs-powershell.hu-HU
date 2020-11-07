---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836717"
---
# <span data-ttu-id="db2a8-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db2a8-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="db2a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="db2a8-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="db2a8-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="db2a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db2a8-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db2a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="db2a8-106">A **Remove-AzVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="db2a8-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="db2a8-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="db2a8-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="db2a8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="db2a8-108">EXAMPLES</span></span>

### <span data-ttu-id="db2a8-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="db2a8-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="db2a8-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="db2a8-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="db2a8-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="db2a8-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="db2a8-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="db2a8-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="db2a8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db2a8-113">PARAMETERS</span></span>

### <span data-ttu-id="db2a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2a8-114">-DefaultProfile</span></span>
<span data-ttu-id="db2a8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db2a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db2a8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db2a8-116">-Name</span></span>
<span data-ttu-id="db2a8-117">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="db2a8-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db2a8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2a8-118">-ResourceGroupName</span></span>
<span data-ttu-id="db2a8-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db2a8-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="db2a8-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="db2a8-120">-VMName</span></span>
<span data-ttu-id="db2a8-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="db2a8-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="db2a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2a8-122">CommonParameters</span></span>
<span data-ttu-id="db2a8-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db2a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2a8-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2a8-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db2a8-125">INPUTS</span></span>

### <span data-ttu-id="db2a8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="db2a8-126">System.String</span></span>

## <span data-ttu-id="db2a8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db2a8-127">OUTPUTS</span></span>

### <span data-ttu-id="db2a8-128">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="db2a8-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="db2a8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db2a8-129">NOTES</span></span>

## <span data-ttu-id="db2a8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db2a8-130">RELATED LINKS</span></span>

[<span data-ttu-id="db2a8-131">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db2a8-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="db2a8-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db2a8-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="db2a8-133">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="db2a8-133">Update-AzVM</span></span>](./Update-AzVM.md)


