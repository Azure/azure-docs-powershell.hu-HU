---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850938"
---
# <span data-ttu-id="3a592-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3a592-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="3a592-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a592-102">SYNOPSIS</span></span>
<span data-ttu-id="3a592-103">Információt kap az egyéni parancsfájl-kiterjesztésről.</span><span class="sxs-lookup"><span data-stu-id="3a592-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a592-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a592-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a592-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a592-105">DESCRIPTION</span></span>
<span data-ttu-id="3a592-106">A **Get-AzureRmVMCustomScriptExtension** parancsmag egy virtuális gépen egy egyéni parancsfájl virtuálisgép-bővítményének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a592-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="3a592-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a592-107">EXAMPLES</span></span>

### <span data-ttu-id="3a592-108">Példa 1: egyéni parancsfájl-kiterjesztés beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a592-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="3a592-109">Ez a parancs a ContosoCustomScript nevű egyéni parancsfájl-kiterjesztést kapja a VirtualMachine07 nevű virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="3a592-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="3a592-110">2. példa: egyéni parancsfájl-kiterjesztés példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a592-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="3a592-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoCustomScript nevű egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a592-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="3a592-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a592-112">PARAMETERS</span></span>

### <span data-ttu-id="3a592-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a592-113">-DefaultProfile</span></span>
<span data-ttu-id="3a592-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a592-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a592-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a592-115">-Name</span></span>
<span data-ttu-id="3a592-116">Annak az egyéni parancsfájlnak a neve, amelyről a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="3a592-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a592-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a592-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a592-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a592-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a592-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="3a592-119">-Status</span></span>
<span data-ttu-id="3a592-120">Jelzi, hogy ez a parancsmag az egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a592-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a592-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a592-121">-VMName</span></span>
<span data-ttu-id="3a592-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag az egyéni parancsfájl-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="3a592-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a592-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a592-123">CommonParameters</span></span>
<span data-ttu-id="3a592-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a592-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a592-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a592-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a592-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a592-126">INPUTS</span></span>

### <span data-ttu-id="3a592-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a592-127">None</span></span>
<span data-ttu-id="3a592-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3a592-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a592-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a592-129">OUTPUTS</span></span>

### <span data-ttu-id="3a592-130">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="3a592-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="3a592-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a592-131">NOTES</span></span>

## <span data-ttu-id="3a592-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a592-132">RELATED LINKS</span></span>

[<span data-ttu-id="3a592-133">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3a592-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3a592-134">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a592-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="3a592-135">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3a592-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


