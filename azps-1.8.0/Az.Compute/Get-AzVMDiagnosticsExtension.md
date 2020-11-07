---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671349"
---
# <span data-ttu-id="296e4-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="296e4-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="296e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="296e4-102">SYNOPSIS</span></span>
<span data-ttu-id="296e4-103">A diagnosztikai bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="296e4-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="296e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="296e4-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="296e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="296e4-105">DESCRIPTION</span></span>
<span data-ttu-id="296e4-106">A **Get-AzVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="296e4-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="296e4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="296e4-107">EXAMPLES</span></span>

### <span data-ttu-id="296e4-108">Példa 1: a diagnosztika bővítmény beszerzése virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="296e4-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="296e4-109">Ez a parancs beilleszti a ContosoVM22 nevű virtuális gépre a diagnosztika bővítményt.</span><span class="sxs-lookup"><span data-stu-id="296e4-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="296e4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="296e4-110">PARAMETERS</span></span>

### <span data-ttu-id="296e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296e4-111">-DefaultProfile</span></span>
<span data-ttu-id="296e4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="296e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="296e4-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="296e4-113">-Name</span></span>
<span data-ttu-id="296e4-114">Annak a diagnosztikai bővítménynek a neve, amelyhez a parancsmag beállításai vannak.</span><span class="sxs-lookup"><span data-stu-id="296e4-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="296e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="296e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="296e4-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="296e4-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="296e4-117">-Állapot</span><span class="sxs-lookup"><span data-stu-id="296e4-117">-Status</span></span>
<span data-ttu-id="296e4-118">Azt jelzi, hogy ez a parancsmag az állapot értékét használja.</span><span class="sxs-lookup"><span data-stu-id="296e4-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="296e4-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="296e4-119">-VMName</span></span>
<span data-ttu-id="296e4-120">Annak a virtuális gépnek a neve, amelyből a parancsmag a diagnosztika bővítményt kapja.</span><span class="sxs-lookup"><span data-stu-id="296e4-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="296e4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296e4-121">CommonParameters</span></span>
<span data-ttu-id="296e4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="296e4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296e4-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="296e4-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296e4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="296e4-124">INPUTS</span></span>

### <span data-ttu-id="296e4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="296e4-125">System.String</span></span>

### <span data-ttu-id="296e4-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="296e4-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="296e4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="296e4-127">OUTPUTS</span></span>

### <span data-ttu-id="296e4-128">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="296e4-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="296e4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="296e4-129">NOTES</span></span>

## <span data-ttu-id="296e4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="296e4-130">RELATED LINKS</span></span>

[<span data-ttu-id="296e4-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="296e4-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="296e4-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="296e4-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


