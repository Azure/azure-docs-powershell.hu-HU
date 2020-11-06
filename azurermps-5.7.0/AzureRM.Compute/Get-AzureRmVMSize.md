---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497723"
---
# <span data-ttu-id="d3416-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="d3416-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="d3416-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3416-102">SYNOPSIS</span></span>
<span data-ttu-id="d3416-103">Elérhetővé válik a virtuális gépek mérete.</span><span class="sxs-lookup"><span data-stu-id="d3416-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3416-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3416-104">SYNTAX</span></span>

### <span data-ttu-id="d3416-105">ListVirtualMachineSizeParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3416-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="d3416-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d3416-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="d3416-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3416-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="d3416-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3416-108">DESCRIPTION</span></span>
<span data-ttu-id="d3416-109">A **Get-AzureRmVMSize** parancsmag a virtuális gépek méreteit érheti el.</span><span class="sxs-lookup"><span data-stu-id="d3416-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="d3416-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3416-110">EXAMPLES</span></span>

### <span data-ttu-id="d3416-111">Példa 1: a virtuális gépek méretének beszerzése egy helyhez</span><span class="sxs-lookup"><span data-stu-id="d3416-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="d3416-112">Ez a parancs a virtuális gépek elérhető méretét a megadott helyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3416-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="d3416-113">2. példa: az elérhetőségi készlet méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3416-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="d3416-114">Ez a parancs elérhetővé válik a virtuális gépek számára, amelyeket a AvailabilitySet17 nevű elérhetőségi készletben lehet telepíteni.</span><span class="sxs-lookup"><span data-stu-id="d3416-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="d3416-115">Példa 3: a meglévő virtuális gép méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3416-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="d3416-116">Ez a parancs elérhetővé válik a meglévő, VirtualMachine12 nevű virtuális gép méretéhez.</span><span class="sxs-lookup"><span data-stu-id="d3416-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="d3416-117">A virtuális gépet átméretezheti a parancs által beolvasott méretben.</span><span class="sxs-lookup"><span data-stu-id="d3416-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="d3416-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3416-118">PARAMETERS</span></span>

### <span data-ttu-id="d3416-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d3416-119">-AvailabilitySetName</span></span>
<span data-ttu-id="d3416-120">Annak az elérhetőségi készletnek a nevét adja meg, amelyhez ez a parancsmag a rendelkezésre álló virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="d3416-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="d3416-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="d3416-121">-Location</span></span>
<span data-ttu-id="d3416-122">Azt a helyet adja meg, ahol ez a parancsmag a rendelkezésre álló virtuális gépek méreteit kapja.</span><span class="sxs-lookup"><span data-stu-id="d3416-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="d3416-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3416-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3416-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3416-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d3416-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="d3416-125">-VMName</span></span>
<span data-ttu-id="d3416-126">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag az átméretezéshez elérhető virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="d3416-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="d3416-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3416-127">CommonParameters</span></span>
<span data-ttu-id="d3416-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3416-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3416-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3416-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3416-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3416-130">INPUTS</span></span>

### <span data-ttu-id="d3416-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3416-131">None</span></span>
<span data-ttu-id="d3416-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d3416-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3416-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3416-133">OUTPUTS</span></span>

## <span data-ttu-id="d3416-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3416-134">NOTES</span></span>

## <span data-ttu-id="d3416-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3416-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3416-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d3416-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


