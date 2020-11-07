---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 46a0ffcaece93328447405f78af2af0785b329c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844558"
---
# <span data-ttu-id="6603d-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="6603d-101">Get-AzVMSize</span></span>

## <span data-ttu-id="6603d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6603d-102">SYNOPSIS</span></span>
<span data-ttu-id="6603d-103">Elérhetővé válik a virtuális gépek mérete.</span><span class="sxs-lookup"><span data-stu-id="6603d-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="6603d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6603d-104">SYNTAX</span></span>

### <span data-ttu-id="6603d-105">ListVirtualMachineSizeParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6603d-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6603d-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6603d-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6603d-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6603d-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6603d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6603d-108">DESCRIPTION</span></span>
<span data-ttu-id="6603d-109">A **Get-AzVMSize** parancsmag a virtuális gépek méreteit érheti el.</span><span class="sxs-lookup"><span data-stu-id="6603d-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="6603d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6603d-110">EXAMPLES</span></span>

### <span data-ttu-id="6603d-111">Példa 1: a virtuális gépek méretének beszerzése egy helyhez</span><span class="sxs-lookup"><span data-stu-id="6603d-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="6603d-112">Ez a parancs a virtuális gépek elérhető méretét a megadott helyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6603d-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="6603d-113">2. példa: az elérhetőségi készlet méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6603d-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="6603d-114">Ez a parancs elérhetővé válik a virtuális gépek számára, amelyeket a AvailabilitySet17 nevű elérhetőségi készletben lehet telepíteni.</span><span class="sxs-lookup"><span data-stu-id="6603d-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="6603d-115">Példa 3: a meglévő virtuális gép méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6603d-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="6603d-116">Ez a parancs elérhetővé válik a meglévő, VirtualMachine12 nevű virtuális gép méretéhez.</span><span class="sxs-lookup"><span data-stu-id="6603d-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="6603d-117">A virtuális gépet átméretezheti a parancs által beolvasott méretben.</span><span class="sxs-lookup"><span data-stu-id="6603d-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="6603d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6603d-118">PARAMETERS</span></span>

### <span data-ttu-id="6603d-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="6603d-119">-AvailabilitySetName</span></span>
<span data-ttu-id="6603d-120">Annak az elérhetőségi készletnek a nevét adja meg, amelyhez ez a parancsmag a rendelkezésre álló virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="6603d-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6603d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6603d-121">-DefaultProfile</span></span>
<span data-ttu-id="6603d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6603d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6603d-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="6603d-123">-Location</span></span>
<span data-ttu-id="6603d-124">Azt a helyet adja meg, ahol ez a parancsmag a rendelkezésre álló virtuális gépek méreteit kapja.</span><span class="sxs-lookup"><span data-stu-id="6603d-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6603d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6603d-125">-ResourceGroupName</span></span>
<span data-ttu-id="6603d-126">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6603d-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6603d-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="6603d-127">-VMName</span></span>
<span data-ttu-id="6603d-128">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag az átméretezéshez elérhető virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="6603d-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6603d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6603d-129">CommonParameters</span></span>
<span data-ttu-id="6603d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6603d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6603d-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6603d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6603d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6603d-132">INPUTS</span></span>

### <span data-ttu-id="6603d-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="6603d-133">None</span></span>
<span data-ttu-id="6603d-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6603d-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6603d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6603d-135">OUTPUTS</span></span>

### <span data-ttu-id="6603d-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="6603d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="6603d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6603d-137">NOTES</span></span>

## <span data-ttu-id="6603d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6603d-138">RELATED LINKS</span></span>

[<span data-ttu-id="6603d-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6603d-139">Get-AzVM</span></span>](./Get-AzVM.md)


