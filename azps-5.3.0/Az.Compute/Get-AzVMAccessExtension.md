---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477817"
---
# <span data-ttu-id="5f451-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5f451-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="5f451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f451-102">SYNOPSIS</span></span>
<span data-ttu-id="5f451-103">Információkat kap a VMAccess bővítményről.</span><span class="sxs-lookup"><span data-stu-id="5f451-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="5f451-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f451-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f451-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f451-105">DESCRIPTION</span></span>
<span data-ttu-id="5f451-106">A **Get-AzVMAccessExtension** parancsmag információkat kap a virtuális gép access (VMAccess) virtuális gép bővítményről.</span><span class="sxs-lookup"><span data-stu-id="5f451-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="5f451-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f451-107">EXAMPLES</span></span>

### <span data-ttu-id="5f451-108">1. példa: A VMAccess bővítmény lekérhetők</span><span class="sxs-lookup"><span data-stu-id="5f451-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="5f451-109">Ez a parancs a ContosoTest nevű VMAccess kiterjesztést kapja a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5f451-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5f451-110">2. példa: A VMAccess bővítmény példánynézetének lekérte</span><span class="sxs-lookup"><span data-stu-id="5f451-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="5f451-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoTest nevű VMAccess bővítményének példánynézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="5f451-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="5f451-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f451-112">PARAMETERS</span></span>

### <span data-ttu-id="5f451-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f451-113">-DefaultProfile</span></span>
<span data-ttu-id="5f451-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f451-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f451-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5f451-115">-Name</span></span>
<span data-ttu-id="5f451-116">Megadja annak a kiterjesztésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5f451-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f451-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f451-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f451-118">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f451-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5f451-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="5f451-119">-Status</span></span>
<span data-ttu-id="5f451-120">Azt jelzi, hogy ez a parancsmag csak a bővítmény példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5f451-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="5f451-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="5f451-121">-VMName</span></span>
<span data-ttu-id="5f451-122">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f451-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5f451-123">Ez a parancsmag információt kap a VMAccess-ről a paraméter által megadott virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5f451-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f451-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f451-124">CommonParameters</span></span>
<span data-ttu-id="5f451-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f451-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f451-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f451-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f451-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f451-127">INPUTS</span></span>

### <span data-ttu-id="5f451-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f451-128">System.String</span></span>

### <span data-ttu-id="5f451-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f451-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f451-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f451-130">OUTPUTS</span></span>

### <span data-ttu-id="5f451-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5f451-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="5f451-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f451-132">NOTES</span></span>

## <span data-ttu-id="5f451-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f451-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f451-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5f451-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="5f451-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5f451-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="5f451-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5f451-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


