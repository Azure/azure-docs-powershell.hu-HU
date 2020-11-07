---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848898"
---
# <span data-ttu-id="3a75a-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3a75a-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3a75a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a75a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a75a-103">Információt kap az VMAccess bővítményről.</span><span class="sxs-lookup"><span data-stu-id="3a75a-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a75a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a75a-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a75a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a75a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a75a-106">A **Get-AzureRmVMAccessExtension** parancsmag információkat kap a Virtual Machine Access (VMAccess) virtuálisgép-bővítményéről.</span><span class="sxs-lookup"><span data-stu-id="3a75a-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="3a75a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a75a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a75a-108">Példa 1: a VMAccess-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a75a-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="3a75a-109">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoTest nevű VMAccess-bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a75a-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="3a75a-110">2. példa: az VMAccess bővítmény példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a75a-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="3a75a-111">Ez a parancs a ContosoTest nevű VMAccess-bővítmény példány nézetét kapja meg a VirtualMachine07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="3a75a-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="3a75a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a75a-112">PARAMETERS</span></span>

### <span data-ttu-id="3a75a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a75a-113">-DefaultProfile</span></span>
<span data-ttu-id="3a75a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a75a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a75a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a75a-115">-Name</span></span>
<span data-ttu-id="3a75a-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3a75a-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3a75a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a75a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a75a-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a75a-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3a75a-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="3a75a-119">-Status</span></span>
<span data-ttu-id="3a75a-120">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a75a-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="3a75a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a75a-121">-VMName</span></span>
<span data-ttu-id="3a75a-122">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a75a-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3a75a-123">Ez a parancsmag információt ad a virtuális gép VMAccess a paraméter által megadott adatokról.</span><span class="sxs-lookup"><span data-stu-id="3a75a-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a75a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a75a-124">CommonParameters</span></span>
<span data-ttu-id="3a75a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a75a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a75a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a75a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a75a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a75a-127">INPUTS</span></span>

### <span data-ttu-id="3a75a-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a75a-128">None</span></span>
<span data-ttu-id="3a75a-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3a75a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a75a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a75a-130">OUTPUTS</span></span>

### <span data-ttu-id="3a75a-131">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="3a75a-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="3a75a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a75a-132">NOTES</span></span>

## <span data-ttu-id="3a75a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a75a-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a75a-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3a75a-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3a75a-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3a75a-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3a75a-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a75a-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


