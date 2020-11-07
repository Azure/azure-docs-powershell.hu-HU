---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: 23120c9225d6905a528ac113bd055ec8fa585870
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844630"
---
# <span data-ttu-id="0425a-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0425a-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="0425a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0425a-102">SYNOPSIS</span></span>
<span data-ttu-id="0425a-103">Információt kap az VMAccess bővítményről.</span><span class="sxs-lookup"><span data-stu-id="0425a-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="0425a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0425a-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0425a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0425a-105">DESCRIPTION</span></span>
<span data-ttu-id="0425a-106">A **Get-AzVMAccessExtension** parancsmag információkat kap a Virtual Machine Access (VMAccess) virtuálisgép-bővítményéről.</span><span class="sxs-lookup"><span data-stu-id="0425a-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="0425a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0425a-107">EXAMPLES</span></span>

### <span data-ttu-id="0425a-108">Példa 1: a VMAccess-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="0425a-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="0425a-109">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoTest nevű VMAccess-bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0425a-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0425a-110">2. példa: az VMAccess bővítmény példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0425a-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="0425a-111">Ez a parancs a ContosoTest nevű VMAccess-bővítmény példány nézetét kapja meg a VirtualMachine07 nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="0425a-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0425a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0425a-112">PARAMETERS</span></span>

### <span data-ttu-id="0425a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0425a-113">-DefaultProfile</span></span>
<span data-ttu-id="0425a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0425a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0425a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0425a-115">-Name</span></span>
<span data-ttu-id="0425a-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="0425a-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0425a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0425a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0425a-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0425a-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0425a-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0425a-119">-Status</span></span>
<span data-ttu-id="0425a-120">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0425a-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="0425a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0425a-121">-VMName</span></span>
<span data-ttu-id="0425a-122">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0425a-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0425a-123">Ez a parancsmag információt ad a virtuális gép VMAccess a paraméter által megadott adatokról.</span><span class="sxs-lookup"><span data-stu-id="0425a-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0425a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0425a-124">CommonParameters</span></span>
<span data-ttu-id="0425a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0425a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0425a-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0425a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0425a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0425a-127">INPUTS</span></span>

### <span data-ttu-id="0425a-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="0425a-128">None</span></span>
<span data-ttu-id="0425a-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0425a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0425a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0425a-130">OUTPUTS</span></span>

### <span data-ttu-id="0425a-131">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0425a-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="0425a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0425a-132">NOTES</span></span>

## <span data-ttu-id="0425a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0425a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0425a-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0425a-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="0425a-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0425a-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="0425a-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0425a-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


