---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 33abc50f4cc336230e1c6f4ef14d12f51b22af83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505992"
---
# <span data-ttu-id="02ca7-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="02ca7-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="02ca7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="02ca7-103">Elérhetővé válik a virtuális gépek mérete.</span><span class="sxs-lookup"><span data-stu-id="02ca7-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02ca7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02ca7-104">SYNTAX</span></span>

### <span data-ttu-id="02ca7-105">ListVirtualMachineSizeParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02ca7-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ca7-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="02ca7-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ca7-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="02ca7-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02ca7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02ca7-108">DESCRIPTION</span></span>
<span data-ttu-id="02ca7-109">A **Get-AzureRmVMSize** parancsmag a virtuális gépek méreteit érheti el.</span><span class="sxs-lookup"><span data-stu-id="02ca7-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="02ca7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02ca7-110">EXAMPLES</span></span>

### <span data-ttu-id="02ca7-111">Példa 1: a virtuális gépek méretének beszerzése egy helyhez</span><span class="sxs-lookup"><span data-stu-id="02ca7-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="02ca7-112">Ez a parancs a virtuális gépek elérhető méretét a megadott helyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02ca7-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="02ca7-113">2. példa: az elérhetőségi készlet méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="02ca7-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="02ca7-114">Ez a parancs elérhetővé válik a virtuális gépek számára, amelyeket a AvailabilitySet17 nevű elérhetőségi készletben lehet telepíteni.</span><span class="sxs-lookup"><span data-stu-id="02ca7-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="02ca7-115">Példa 3: a meglévő virtuális gép méretének beszerzése</span><span class="sxs-lookup"><span data-stu-id="02ca7-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="02ca7-116">Ez a parancs elérhetővé válik a meglévő, VirtualMachine12 nevű virtuális gép méretéhez.</span><span class="sxs-lookup"><span data-stu-id="02ca7-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="02ca7-117">A virtuális gépet átméretezheti a parancs által beolvasott méretben.</span><span class="sxs-lookup"><span data-stu-id="02ca7-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="02ca7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02ca7-118">PARAMETERS</span></span>

### <span data-ttu-id="02ca7-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="02ca7-119">-AvailabilitySetName</span></span>
<span data-ttu-id="02ca7-120">Annak az elérhetőségi készletnek a nevét adja meg, amelyhez ez a parancsmag a rendelkezésre álló virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="02ca7-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="02ca7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ca7-121">-DefaultProfile</span></span>
<span data-ttu-id="02ca7-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02ca7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ca7-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="02ca7-123">-Location</span></span>
<span data-ttu-id="02ca7-124">Azt a helyet adja meg, ahol ez a parancsmag a rendelkezésre álló virtuális gépek méreteit kapja.</span><span class="sxs-lookup"><span data-stu-id="02ca7-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="02ca7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ca7-125">-ResourceGroupName</span></span>
<span data-ttu-id="02ca7-126">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02ca7-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="02ca7-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="02ca7-127">-VMName</span></span>
<span data-ttu-id="02ca7-128">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag az átméretezéshez elérhető virtuális gépek méretét kapja.</span><span class="sxs-lookup"><span data-stu-id="02ca7-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="02ca7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ca7-129">CommonParameters</span></span>
<span data-ttu-id="02ca7-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02ca7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ca7-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ca7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ca7-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ca7-132">INPUTS</span></span>

## <span data-ttu-id="02ca7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ca7-133">OUTPUTS</span></span>

## <span data-ttu-id="02ca7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02ca7-134">NOTES</span></span>

## <span data-ttu-id="02ca7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02ca7-135">RELATED LINKS</span></span>

[<span data-ttu-id="02ca7-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="02ca7-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


