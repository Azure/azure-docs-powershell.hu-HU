---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496636"
---
# <span data-ttu-id="a0b78-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0b78-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a0b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0b78-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b78-103">A diagnosztikai bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0b78-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0b78-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="a0b78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0b78-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b78-106">A **Get-AzureRmVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0b78-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a0b78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0b78-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b78-108">Példa 1: a diagnosztika bővítmény beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="a0b78-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a0b78-109">Ez a parancs beilleszti a ContosoVM22 nevű virtuális gépre a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a0b78-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a0b78-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0b78-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b78-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0b78-111">-Name</span></span>
<span data-ttu-id="a0b78-112">Annak a diagnosztikai bővítménynek a neve, amelyhez a parancsmag beállításai vannak.</span><span class="sxs-lookup"><span data-stu-id="a0b78-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a0b78-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b78-113">-ResourceGroupName</span></span>
<span data-ttu-id="a0b78-114">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0b78-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a0b78-115">-Állapot</span><span class="sxs-lookup"><span data-stu-id="a0b78-115">-Status</span></span>
<span data-ttu-id="a0b78-116">Azt jelzi, hogy ez a parancsmag az állapot értékét használja.</span><span class="sxs-lookup"><span data-stu-id="a0b78-116">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b78-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a0b78-117">-VMName</span></span>
<span data-ttu-id="a0b78-118">Annak a virtuális gépnek a neve, amelyből a parancsmag a diagnosztika bővítményt kapja.</span><span class="sxs-lookup"><span data-stu-id="a0b78-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a0b78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b78-119">CommonParameters</span></span>
<span data-ttu-id="a0b78-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0b78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b78-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b78-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b78-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b78-122">INPUTS</span></span>

### <span data-ttu-id="a0b78-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0b78-123">None</span></span>
<span data-ttu-id="a0b78-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a0b78-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0b78-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b78-125">OUTPUTS</span></span>

## <span data-ttu-id="a0b78-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0b78-126">NOTES</span></span>

## <span data-ttu-id="a0b78-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0b78-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0b78-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0b78-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="a0b78-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0b78-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


