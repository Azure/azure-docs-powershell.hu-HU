---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015053"
---
# <span data-ttu-id="bc382-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="bc382-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="bc382-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc382-102">SYNOPSIS</span></span>
<span data-ttu-id="bc382-103">Információt kap az egyéni parancsfájl-kiterjesztésről.</span><span class="sxs-lookup"><span data-stu-id="bc382-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="bc382-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc382-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc382-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc382-105">DESCRIPTION</span></span>
<span data-ttu-id="bc382-106">A **Get-AzVMCustomScriptExtension** parancsmag egy virtuális gépen egy egyéni parancsfájl virtuálisgép-bővítményének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc382-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="bc382-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc382-107">EXAMPLES</span></span>

### <span data-ttu-id="bc382-108">Példa 1: egyéni parancsfájl-kiterjesztés beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc382-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="bc382-109">Ez a parancs a ContosoCustomScript nevű egyéni parancsfájl-kiterjesztést kapja a VirtualMachine07 nevű virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="bc382-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="bc382-110">2. példa: egyéni parancsfájl-kiterjesztés példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc382-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="bc382-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoCustomScript nevű egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc382-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="bc382-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc382-112">PARAMETERS</span></span>

### <span data-ttu-id="bc382-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc382-113">-DefaultProfile</span></span>
<span data-ttu-id="bc382-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc382-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc382-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc382-115">-Name</span></span>
<span data-ttu-id="bc382-116">Annak az egyéni parancsfájlnak a neve, amelyről a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="bc382-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="bc382-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc382-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc382-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc382-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bc382-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="bc382-119">-Status</span></span>
<span data-ttu-id="bc382-120">Jelzi, hogy ez a parancsmag az egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc382-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="bc382-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="bc382-121">-VMName</span></span>
<span data-ttu-id="bc382-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag az egyéni parancsfájl-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="bc382-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="bc382-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc382-123">CommonParameters</span></span>
<span data-ttu-id="bc382-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc382-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc382-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc382-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc382-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc382-126">INPUTS</span></span>

### <span data-ttu-id="bc382-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bc382-127">System.String</span></span>

### <span data-ttu-id="bc382-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc382-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc382-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc382-129">OUTPUTS</span></span>

### <span data-ttu-id="bc382-130">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="bc382-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="bc382-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc382-131">NOTES</span></span>

## <span data-ttu-id="bc382-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc382-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc382-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bc382-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="bc382-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="bc382-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="bc382-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="bc382-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


