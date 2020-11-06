---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495427"
---
# <span data-ttu-id="8a636-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a636-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="8a636-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a636-102">SYNOPSIS</span></span>
<span data-ttu-id="8a636-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="8a636-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a636-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a636-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a636-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a636-105">DESCRIPTION</span></span>
<span data-ttu-id="8a636-106">A **Remove-AzureRmVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="8a636-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="8a636-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8a636-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="8a636-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8a636-108">EXAMPLES</span></span>

### <span data-ttu-id="8a636-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="8a636-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="8a636-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8a636-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="8a636-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8a636-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a636-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="8a636-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="8a636-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a636-113">PARAMETERS</span></span>

### <span data-ttu-id="8a636-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a636-114">-Name</span></span>
<span data-ttu-id="8a636-115">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="8a636-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a636-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a636-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a636-117">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a636-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8a636-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="8a636-118">-VMName</span></span>
<span data-ttu-id="8a636-119">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8a636-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="8a636-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a636-120">CommonParameters</span></span>
<span data-ttu-id="8a636-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a636-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a636-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a636-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a636-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a636-123">INPUTS</span></span>

### <span data-ttu-id="8a636-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a636-124">None</span></span>
<span data-ttu-id="8a636-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8a636-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a636-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a636-126">OUTPUTS</span></span>

## <span data-ttu-id="8a636-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a636-127">NOTES</span></span>

## <span data-ttu-id="8a636-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a636-128">RELATED LINKS</span></span>

[<span data-ttu-id="8a636-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a636-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="8a636-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a636-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="8a636-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a636-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


