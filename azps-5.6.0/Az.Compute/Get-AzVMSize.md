---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: b669d415e88c16f7ddfe532f05bc754561b7ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933090"
---
# <span data-ttu-id="37b74-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="37b74-101">Get-AzVMSize</span></span>

## <span data-ttu-id="37b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b74-102">SYNOPSIS</span></span>
<span data-ttu-id="37b74-103">Elérhetővé válik virtuális gépméretek.</span><span class="sxs-lookup"><span data-stu-id="37b74-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="37b74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37b74-104">SYNTAX</span></span>

### <span data-ttu-id="37b74-105">ListVirtualMachineSizeParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37b74-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37b74-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37b74-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37b74-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="37b74-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37b74-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37b74-108">DESCRIPTION</span></span>
<span data-ttu-id="37b74-109">A **Get-AzVMSize parancsmag** elérhetővé válik virtuális gépméretekben.</span><span class="sxs-lookup"><span data-stu-id="37b74-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="37b74-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37b74-110">EXAMPLES</span></span>

### <span data-ttu-id="37b74-111">1. példa: Virtuális gépméretek lekérte egy helyhez</span><span class="sxs-lookup"><span data-stu-id="37b74-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="37b74-112">Ez a parancs a megadott helyen lévő virtuális gépekhez elérhető méreteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="37b74-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="37b74-113">2. példa: Elérhetőségi készlet méretei</span><span class="sxs-lookup"><span data-stu-id="37b74-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="37b74-114">Ez a parancs elérhető méretű virtuális gépekhez, amelyek telepíthetők az ElérhetőségiKészlet17 nevű rendelkezésre állási halmazban.</span><span class="sxs-lookup"><span data-stu-id="37b74-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="37b74-115">3. példa: Meglévő virtuális gép méretének lekérte</span><span class="sxs-lookup"><span data-stu-id="37b74-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="37b74-116">Ez a parancs elérhető lesz a VirtualMachine12 nevű meglévő virtuális gép méretekhez.</span><span class="sxs-lookup"><span data-stu-id="37b74-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="37b74-117">Ezt a virtuális gépet átméretezheti a parancs méretének megfelelőre.</span><span class="sxs-lookup"><span data-stu-id="37b74-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="37b74-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37b74-118">PARAMETERS</span></span>

### <span data-ttu-id="37b74-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="37b74-119">-AvailabilitySetName</span></span>
<span data-ttu-id="37b74-120">Annak az elérhetőségi halmaznak a nevét adja meg, amelynek a parancsmagja a rendelkezésre álló virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="37b74-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="37b74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b74-121">-DefaultProfile</span></span>
<span data-ttu-id="37b74-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37b74-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b74-123">-Location</span><span class="sxs-lookup"><span data-stu-id="37b74-123">-Location</span></span>
<span data-ttu-id="37b74-124">Azt a helyet adja meg, ahol a parancsmag a rendelkezésre álló virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="37b74-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="37b74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b74-125">-ResourceGroupName</span></span>
<span data-ttu-id="37b74-126">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="37b74-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="37b74-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="37b74-127">-VMName</span></span>
<span data-ttu-id="37b74-128">Megadja annak a virtuális gépnek a nevét, amelybe ez a parancsmag az átméretezéshez elérhető virtuális gépméreteket kapja.</span><span class="sxs-lookup"><span data-stu-id="37b74-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="37b74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b74-129">CommonParameters</span></span>
<span data-ttu-id="37b74-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b74-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37b74-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b74-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37b74-132">INPUTS</span></span>

### <span data-ttu-id="37b74-133">System.String</span><span class="sxs-lookup"><span data-stu-id="37b74-133">System.String</span></span>

## <span data-ttu-id="37b74-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37b74-134">OUTPUTS</span></span>

### <span data-ttu-id="37b74-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="37b74-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="37b74-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37b74-136">NOTES</span></span>

## <span data-ttu-id="37b74-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37b74-137">RELATED LINKS</span></span>

[<span data-ttu-id="37b74-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="37b74-138">Get-AzVM</span></span>](./Get-AzVM.md)


