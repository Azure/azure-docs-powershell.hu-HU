---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849753"
---
# <span data-ttu-id="2fc8f-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2fc8f-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="2fc8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc8f-103">Eltávolítja a diagnosztikai bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fc8f-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fc8f-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc8f-106">A **Remove-AzureRmVMDiagnosticsExtension** parancsmag eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="2fc8f-107">A módosítások végrehajtásához át kell adnia a parancsmag kimenetét a Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="2fc8f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2fc8f-108">EXAMPLES</span></span>

### <span data-ttu-id="2fc8f-109">1. példa: a diagnosztikai bővítmény eltávolítása egy virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="2fc8f-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="2fc8f-110">Ez a parancs eltávolítja a ContosoVM22 nevű virtuális gépről a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="2fc8f-111">A parancs a csővezeték-kezelő használatával átadja az eredményt az Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2fc8f-112">A parancs frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="2fc8f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fc8f-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc8f-114">-DefaultProfile</span></span>
<span data-ttu-id="2fc8f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc8f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2fc8f-116">-Name</span></span>
<span data-ttu-id="2fc8f-117">Itt adhatja meg annak a diagnosztikai bővítménynek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2fc8f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc8f-118">-ResourceGroupName</span></span>
<span data-ttu-id="2fc8f-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2fc8f-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="2fc8f-120">-VMName</span></span>
<span data-ttu-id="2fc8f-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="2fc8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc8f-122">CommonParameters</span></span>
<span data-ttu-id="2fc8f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fc8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc8f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc8f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc8f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fc8f-125">INPUTS</span></span>

### <span data-ttu-id="2fc8f-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="2fc8f-126">None</span></span>
<span data-ttu-id="2fc8f-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2fc8f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fc8f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fc8f-128">OUTPUTS</span></span>

### <span data-ttu-id="2fc8f-129">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2fc8f-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2fc8f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fc8f-130">NOTES</span></span>

## <span data-ttu-id="2fc8f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fc8f-131">RELATED LINKS</span></span>

[<span data-ttu-id="2fc8f-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2fc8f-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="2fc8f-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2fc8f-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="2fc8f-134">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2fc8f-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


