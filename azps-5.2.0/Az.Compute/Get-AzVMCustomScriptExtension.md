---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353862"
---
# <span data-ttu-id="72f59-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72f59-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="72f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f59-102">SYNOPSIS</span></span>
<span data-ttu-id="72f59-103">Információkat kap egy egyéni parancsfájl-kiterjesztésről.</span><span class="sxs-lookup"><span data-stu-id="72f59-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="72f59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72f59-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f59-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72f59-105">DESCRIPTION</span></span>
<span data-ttu-id="72f59-106">A **Get-AzVMCustomScriptExtension** parancsmag információt kap egy virtuális gépen futtatott egyéni parancsfájl virtuális gépbővítményről.</span><span class="sxs-lookup"><span data-stu-id="72f59-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="72f59-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72f59-107">EXAMPLES</span></span>

### <span data-ttu-id="72f59-108">1. példa: Egyéni parancsprogram-bővítmény létrehozása</span><span class="sxs-lookup"><span data-stu-id="72f59-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="72f59-109">Ez a parancs a ContosoCustomScript nevű egyéni parancsfájlkiterjesztést kapja a VirtualMachine07 nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="72f59-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="72f59-110">2. példa: Egyéni parancsfájlbővítmény példánynézetének lekérte</span><span class="sxs-lookup"><span data-stu-id="72f59-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="72f59-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoCustomScript nevű egyéni parancsfájl-bővítményének példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72f59-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="72f59-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72f59-112">PARAMETERS</span></span>

### <span data-ttu-id="72f59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f59-113">-DefaultProfile</span></span>
<span data-ttu-id="72f59-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72f59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72f59-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72f59-115">-Name</span></span>
<span data-ttu-id="72f59-116">Annak az egyéni parancsprogram-bővítménynek a nevét adja meg, amelyről a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="72f59-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="72f59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f59-117">-ResourceGroupName</span></span>
<span data-ttu-id="72f59-118">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72f59-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="72f59-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="72f59-119">-Status</span></span>
<span data-ttu-id="72f59-120">Azt jelzi, hogy ez a parancsmag az egyéni parancsprogram-bővítmény példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72f59-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="72f59-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="72f59-121">-VMName</span></span>
<span data-ttu-id="72f59-122">Annak a virtuális gépnek a nevét adja meg, amelyhez a parancsmag egyéni parancsprogram-kiterjesztést kap.</span><span class="sxs-lookup"><span data-stu-id="72f59-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="72f59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f59-123">CommonParameters</span></span>
<span data-ttu-id="72f59-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f59-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72f59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f59-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72f59-126">INPUTS</span></span>

### <span data-ttu-id="72f59-127">System.String</span><span class="sxs-lookup"><span data-stu-id="72f59-127">System.String</span></span>

### <span data-ttu-id="72f59-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72f59-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72f59-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72f59-129">OUTPUTS</span></span>

### <span data-ttu-id="72f59-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="72f59-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="72f59-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72f59-131">NOTES</span></span>

## <span data-ttu-id="72f59-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72f59-132">RELATED LINKS</span></span>

[<span data-ttu-id="72f59-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="72f59-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="72f59-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="72f59-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="72f59-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="72f59-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


