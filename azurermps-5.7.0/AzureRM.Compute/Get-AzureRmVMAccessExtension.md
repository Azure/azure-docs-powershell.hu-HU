---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494558"
---
# <span data-ttu-id="42989-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="42989-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="42989-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42989-102">SYNOPSIS</span></span>
<span data-ttu-id="42989-103">Információt kap az VMAccess bővítményről.</span><span class="sxs-lookup"><span data-stu-id="42989-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42989-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42989-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="42989-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42989-105">DESCRIPTION</span></span>
<span data-ttu-id="42989-106">A **Get-AzureRmVMAccessExtension** parancsmag információkat kap a Virtual Machine Access (VMAccess) virtuálisgép-bővítményéről.</span><span class="sxs-lookup"><span data-stu-id="42989-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="42989-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42989-107">EXAMPLES</span></span>

### <span data-ttu-id="42989-108">Példa 1: a VMAccess-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="42989-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="42989-109">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoTest nevű VMAccess-bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42989-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="42989-110">2. példa: az VMAccess bővítmény példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="42989-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="42989-111">Ez a parancs a ContosoTest nevű VMAccess-bővítmény példány nézetét kapja meg a VirtualMachine07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="42989-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="42989-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42989-112">PARAMETERS</span></span>

### <span data-ttu-id="42989-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42989-113">-Name</span></span>
<span data-ttu-id="42989-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="42989-114">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="42989-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42989-115">-ResourceGroupName</span></span>
<span data-ttu-id="42989-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42989-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42989-117">-Állapot</span><span class="sxs-lookup"><span data-stu-id="42989-117">-Status</span></span>
<span data-ttu-id="42989-118">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42989-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="42989-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="42989-119">-VMName</span></span>
<span data-ttu-id="42989-120">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42989-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="42989-121">Ez a parancsmag információt ad a virtuális gép VMAccess a paraméter által megadott adatokról.</span><span class="sxs-lookup"><span data-stu-id="42989-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="42989-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42989-122">CommonParameters</span></span>
<span data-ttu-id="42989-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42989-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42989-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42989-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42989-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42989-125">INPUTS</span></span>

### <span data-ttu-id="42989-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="42989-126">None</span></span>
<span data-ttu-id="42989-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="42989-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42989-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42989-128">OUTPUTS</span></span>

## <span data-ttu-id="42989-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42989-129">NOTES</span></span>

## <span data-ttu-id="42989-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42989-130">RELATED LINKS</span></span>

[<span data-ttu-id="42989-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="42989-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="42989-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="42989-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="42989-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="42989-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


