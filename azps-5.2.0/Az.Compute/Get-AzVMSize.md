---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369471"
---
# <span data-ttu-id="43b85-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="43b85-101">Get-AzVMSize</span></span>

## <span data-ttu-id="43b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43b85-102">SYNOPSIS</span></span>
<span data-ttu-id="43b85-103">Elérhetővé válik virtuális gépméretek.</span><span class="sxs-lookup"><span data-stu-id="43b85-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="43b85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43b85-104">SYNTAX</span></span>

### <span data-ttu-id="43b85-105">ListVirtualMachineSizeParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43b85-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b85-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="43b85-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b85-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="43b85-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43b85-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43b85-108">DESCRIPTION</span></span>
<span data-ttu-id="43b85-109">A **Get-AzVMSize parancsmag** elérhetővé válik virtuális gépméretekben.</span><span class="sxs-lookup"><span data-stu-id="43b85-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="43b85-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43b85-110">EXAMPLES</span></span>

### <span data-ttu-id="43b85-111">1. példa: Virtuális gépméretek lekérte egy helyhez</span><span class="sxs-lookup"><span data-stu-id="43b85-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="43b85-112">Ez a parancs a megadott helyen lévő virtuális gépekhez elérhető méreteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43b85-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="43b85-113">2. példa: Elérhetőségi készlet méretei</span><span class="sxs-lookup"><span data-stu-id="43b85-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="43b85-114">Ez a parancs elérhető méretű virtuális gépekhez, amelyek telepíthetők az ElérhetőségiKészlet17 nevű rendelkezésre állási halmazban.</span><span class="sxs-lookup"><span data-stu-id="43b85-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="43b85-115">3. példa: Meglévő virtuális gép méretének lekérte</span><span class="sxs-lookup"><span data-stu-id="43b85-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="43b85-116">Ez a parancs elérhető méretű lesz a VirtualMachine12 nevű meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="43b85-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="43b85-117">Ezt a virtuális gépet átméretezheti a parancs méretének megfelelőre.</span><span class="sxs-lookup"><span data-stu-id="43b85-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="43b85-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43b85-118">PARAMETERS</span></span>

### <span data-ttu-id="43b85-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="43b85-119">-AvailabilitySetName</span></span>
<span data-ttu-id="43b85-120">Annak az elérhetőségi halmaznak a nevét adja meg, amelynek a parancsmagja a rendelkezésre álló virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="43b85-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b85-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b85-121">-DefaultProfile</span></span>
<span data-ttu-id="43b85-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43b85-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b85-123">-Location</span><span class="sxs-lookup"><span data-stu-id="43b85-123">-Location</span></span>
<span data-ttu-id="43b85-124">Azt a helyet adja meg, ahol a parancsmag a rendelkezésre álló virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="43b85-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b85-125">-ResourceGroupName</span></span>
<span data-ttu-id="43b85-126">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43b85-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b85-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="43b85-127">-VMName</span></span>
<span data-ttu-id="43b85-128">Megadja annak a virtuális gépnek a nevét, amelybe ez a parancsmag az átméretezéshez elérhető virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="43b85-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b85-129">CommonParameters</span></span>
<span data-ttu-id="43b85-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b85-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43b85-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b85-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43b85-132">INPUTS</span></span>

### <span data-ttu-id="43b85-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43b85-133">System.String</span></span>

## <span data-ttu-id="43b85-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43b85-134">OUTPUTS</span></span>

### <span data-ttu-id="43b85-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="43b85-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="43b85-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43b85-136">NOTES</span></span>

## <span data-ttu-id="43b85-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43b85-137">RELATED LINKS</span></span>

[<span data-ttu-id="43b85-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="43b85-138">Get-AzVM</span></span>](./Get-AzVM.md)


