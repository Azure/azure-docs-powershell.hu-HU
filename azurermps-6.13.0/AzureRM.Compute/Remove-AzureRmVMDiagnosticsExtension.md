---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502204"
---
# <span data-ttu-id="a4d12-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4d12-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a4d12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4d12-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d12-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a4d12-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4d12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4d12-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4d12-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4d12-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d12-106">A **Remove-AzureRmVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a4d12-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="a4d12-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a4d12-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="a4d12-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a4d12-108">EXAMPLES</span></span>

### <span data-ttu-id="a4d12-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="a4d12-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="a4d12-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a4d12-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="a4d12-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a4d12-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a4d12-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a4d12-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="a4d12-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4d12-113">PARAMETERS</span></span>

### <span data-ttu-id="a4d12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d12-114">-DefaultProfile</span></span>
<span data-ttu-id="a4d12-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4d12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d12-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4d12-116">-Name</span></span>
<span data-ttu-id="a4d12-117">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="a4d12-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a4d12-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d12-118">-ResourceGroupName</span></span>
<span data-ttu-id="a4d12-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4d12-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a4d12-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4d12-120">-VMName</span></span>
<span data-ttu-id="a4d12-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a4d12-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="a4d12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d12-122">CommonParameters</span></span>
<span data-ttu-id="a4d12-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4d12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d12-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d12-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d12-125">INPUTS</span></span>

### <span data-ttu-id="a4d12-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d12-126">System.String</span></span>

## <span data-ttu-id="a4d12-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d12-127">OUTPUTS</span></span>

### <span data-ttu-id="a4d12-128">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a4d12-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a4d12-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4d12-129">NOTES</span></span>

## <span data-ttu-id="a4d12-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4d12-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4d12-131">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4d12-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="a4d12-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4d12-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="a4d12-133">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4d12-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

