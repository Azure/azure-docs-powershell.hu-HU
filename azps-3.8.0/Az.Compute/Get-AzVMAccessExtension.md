---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015059"
---
# <span data-ttu-id="d6b55-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d6b55-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="d6b55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6b55-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b55-103">Információt kap az VMAccess bővítményről.</span><span class="sxs-lookup"><span data-stu-id="d6b55-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="d6b55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6b55-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6b55-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b55-106">A **Get-AzVMAccessExtension** parancsmag információkat kap a Virtual Machine Access (VMAccess) virtuálisgép-bővítményéről.</span><span class="sxs-lookup"><span data-stu-id="d6b55-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="d6b55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6b55-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b55-108">Példa 1: a VMAccess-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6b55-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="d6b55-109">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoTest nevű VMAccess-bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d6b55-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d6b55-110">2. példa: az VMAccess bővítmény példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6b55-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="d6b55-111">Ez a parancs a ContosoTest nevű VMAccess-bővítmény példány nézetét kapja meg a VirtualMachine07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d6b55-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d6b55-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6b55-112">PARAMETERS</span></span>

### <span data-ttu-id="d6b55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b55-113">-DefaultProfile</span></span>
<span data-ttu-id="d6b55-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6b55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6b55-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6b55-115">-Name</span></span>
<span data-ttu-id="d6b55-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d6b55-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b55-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b55-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6b55-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6b55-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d6b55-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d6b55-119">-Status</span></span>
<span data-ttu-id="d6b55-120">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d6b55-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="d6b55-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d6b55-121">-VMName</span></span>
<span data-ttu-id="d6b55-122">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6b55-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d6b55-123">Ez a parancsmag információt ad a virtuális gép VMAccess a paraméter által megadott adatokról.</span><span class="sxs-lookup"><span data-stu-id="d6b55-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6b55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b55-124">CommonParameters</span></span>
<span data-ttu-id="d6b55-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6b55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b55-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6b55-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b55-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6b55-127">INPUTS</span></span>

### <span data-ttu-id="d6b55-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6b55-128">System.String</span></span>

### <span data-ttu-id="d6b55-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6b55-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6b55-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6b55-130">OUTPUTS</span></span>

### <span data-ttu-id="d6b55-131">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d6b55-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="d6b55-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6b55-132">NOTES</span></span>

## <span data-ttu-id="d6b55-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6b55-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6b55-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d6b55-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="d6b55-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d6b55-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="d6b55-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d6b55-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


