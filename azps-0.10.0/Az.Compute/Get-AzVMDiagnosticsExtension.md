---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844618"
---
# <span data-ttu-id="27a1d-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27a1d-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="27a1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="27a1d-103">A diagnosztikai bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27a1d-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="27a1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27a1d-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27a1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="27a1d-106">A **Get-AzVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27a1d-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="27a1d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27a1d-107">EXAMPLES</span></span>

### <span data-ttu-id="27a1d-108">Példa 1: a diagnosztika bővítmény beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="27a1d-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="27a1d-109">Ez a parancs beilleszti a ContosoVM22 nevű virtuális gépre a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27a1d-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="27a1d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27a1d-110">PARAMETERS</span></span>

### <span data-ttu-id="27a1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a1d-111">-DefaultProfile</span></span>
<span data-ttu-id="27a1d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27a1d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a1d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27a1d-113">-Name</span></span>
<span data-ttu-id="27a1d-114">Annak a diagnosztikai bővítménynek a neve, amelyhez a parancsmag beállításai vannak.</span><span class="sxs-lookup"><span data-stu-id="27a1d-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="27a1d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a1d-115">-ResourceGroupName</span></span>
<span data-ttu-id="27a1d-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27a1d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="27a1d-117">-Állapot</span><span class="sxs-lookup"><span data-stu-id="27a1d-117">-Status</span></span>
<span data-ttu-id="27a1d-118">Azt jelzi, hogy ez a parancsmag az állapot értékét használja.</span><span class="sxs-lookup"><span data-stu-id="27a1d-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="27a1d-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="27a1d-119">-VMName</span></span>
<span data-ttu-id="27a1d-120">Annak a virtuális gépnek a neve, amelyből a parancsmag a diagnosztika bővítményt kapja.</span><span class="sxs-lookup"><span data-stu-id="27a1d-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="27a1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a1d-121">CommonParameters</span></span>
<span data-ttu-id="27a1d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27a1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a1d-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a1d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a1d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a1d-124">INPUTS</span></span>

### <span data-ttu-id="27a1d-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="27a1d-125">None</span></span>
<span data-ttu-id="27a1d-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="27a1d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27a1d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a1d-127">OUTPUTS</span></span>

### <span data-ttu-id="27a1d-128">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="27a1d-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="27a1d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27a1d-129">NOTES</span></span>

## <span data-ttu-id="27a1d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27a1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="27a1d-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27a1d-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="27a1d-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27a1d-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


