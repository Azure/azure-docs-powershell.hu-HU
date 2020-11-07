---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: add3437794430e0d5e41ab9330072db4ac3e1616
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836789"
---
# <span data-ttu-id="b762d-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b762d-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="b762d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b762d-102">SYNOPSIS</span></span>
<span data-ttu-id="b762d-103">Információt kap az egyéni parancsfájl-kiterjesztésről.</span><span class="sxs-lookup"><span data-stu-id="b762d-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="b762d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b762d-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b762d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b762d-105">DESCRIPTION</span></span>
<span data-ttu-id="b762d-106">A **Get-AzVMCustomScriptExtension** parancsmag egy virtuális gépen egy egyéni parancsfájl virtuálisgép-bővítményének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b762d-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="b762d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b762d-107">EXAMPLES</span></span>

### <span data-ttu-id="b762d-108">Példa 1: egyéni parancsfájl-kiterjesztés beszerzése</span><span class="sxs-lookup"><span data-stu-id="b762d-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="b762d-109">Ez a parancs a ContosoCustomScript nevű egyéni parancsfájl-kiterjesztést kapja a VirtualMachine07 nevű virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="b762d-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b762d-110">2. példa: egyéni parancsfájl-kiterjesztés példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="b762d-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="b762d-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoCustomScript nevű egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b762d-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="b762d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b762d-112">PARAMETERS</span></span>

### <span data-ttu-id="b762d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b762d-113">-DefaultProfile</span></span>
<span data-ttu-id="b762d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b762d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b762d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b762d-115">-Name</span></span>
<span data-ttu-id="b762d-116">Annak az egyéni parancsfájlnak a neve, amelyről a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="b762d-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="b762d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b762d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b762d-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b762d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b762d-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="b762d-119">-Status</span></span>
<span data-ttu-id="b762d-120">Jelzi, hogy ez a parancsmag az egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b762d-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="b762d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="b762d-121">-VMName</span></span>
<span data-ttu-id="b762d-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag az egyéni parancsfájl-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="b762d-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="b762d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b762d-123">CommonParameters</span></span>
<span data-ttu-id="b762d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b762d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b762d-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b762d-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b762d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b762d-126">INPUTS</span></span>

### <span data-ttu-id="b762d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b762d-127">System.String</span></span>

### <span data-ttu-id="b762d-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b762d-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b762d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b762d-129">OUTPUTS</span></span>

### <span data-ttu-id="b762d-130">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b762d-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="b762d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b762d-131">NOTES</span></span>

## <span data-ttu-id="b762d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b762d-132">RELATED LINKS</span></span>

[<span data-ttu-id="b762d-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b762d-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="b762d-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b762d-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="b762d-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b762d-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


