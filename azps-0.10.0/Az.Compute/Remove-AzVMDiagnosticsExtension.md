---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844377"
---
# <span data-ttu-id="3e4b9-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3e4b9-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3e4b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4b9-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="3e4b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e4b9-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e4b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4b9-106">A **Remove-AzVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3e4b9-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3e4b9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3e4b9-108">EXAMPLES</span></span>

### <span data-ttu-id="3e4b9-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="3e4b9-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="3e4b9-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3e4b9-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3e4b9-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3e4b9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e4b9-113">PARAMETERS</span></span>

### <span data-ttu-id="3e4b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4b9-114">-DefaultProfile</span></span>
<span data-ttu-id="3e4b9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4b9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e4b9-116">-Name</span></span>
<span data-ttu-id="3e4b9-117">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="3e4b9-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4b9-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e4b9-120">-VMName</span></span>
<span data-ttu-id="3e4b9-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4b9-122">CommonParameters</span></span>
<span data-ttu-id="3e4b9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e4b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4b9-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4b9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4b9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e4b9-125">INPUTS</span></span>

### <span data-ttu-id="3e4b9-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e4b9-126">None</span></span>
<span data-ttu-id="3e4b9-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3e4b9-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e4b9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e4b9-128">OUTPUTS</span></span>

### <span data-ttu-id="3e4b9-129">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3e4b9-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e4b9-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e4b9-130">NOTES</span></span>

## <span data-ttu-id="3e4b9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e4b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e4b9-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3e4b9-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3e4b9-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3e4b9-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3e4b9-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e4b9-134">Update-AzVM</span></span>](./Update-AzVM.md)


