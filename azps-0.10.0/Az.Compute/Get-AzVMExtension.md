---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844601"
---
# <span data-ttu-id="315f7-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="315f7-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="315f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="315f7-102">SYNOPSIS</span></span>
<span data-ttu-id="315f7-103">A virtuálisgép-bővítmények tulajdonságait a virtuális gépen telepítette.</span><span class="sxs-lookup"><span data-stu-id="315f7-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="315f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="315f7-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="315f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="315f7-105">DESCRIPTION</span></span>
<span data-ttu-id="315f7-106">A **Get-AzVMExtension** parancsmag a virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="315f7-107">Adja meg annak a bővítménynek a nevét, amelyhez tulajdonságokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="315f7-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="315f7-108">Ha csak a bővítmény példány nézetét szeretné látni, adja meg az állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="315f7-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="315f7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="315f7-109">EXAMPLES</span></span>

### <span data-ttu-id="315f7-110">Példa 1: bővítmény tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="315f7-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="315f7-111">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait az erőforráscsoport ResourceGroup11 VirtualMachine22 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="315f7-112">2. példa: egy bővítmény példány nézetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="315f7-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="315f7-113">Ez a parancs a CustomScriptExtension nevű VirtualMachine22 nevű virtuális gép példány nézetét kapja meg az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="315f7-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="315f7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="315f7-114">PARAMETERS</span></span>

### <span data-ttu-id="315f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315f7-115">-DefaultProfile</span></span>
<span data-ttu-id="315f7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="315f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315f7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="315f7-117">-Name</span></span>
<span data-ttu-id="315f7-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="315f7-119">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="315f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="315f7-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="315f7-122">-Állapot</span><span class="sxs-lookup"><span data-stu-id="315f7-122">-Status</span></span>
<span data-ttu-id="315f7-123">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="315f7-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="315f7-124">-VMName</span></span>
<span data-ttu-id="315f7-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="315f7-126">Ez a parancsmag a virtuális gép egy bővítményének tulajdonságait adja meg, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="315f7-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="315f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315f7-127">CommonParameters</span></span>
<span data-ttu-id="315f7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="315f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315f7-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="315f7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315f7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="315f7-130">INPUTS</span></span>

### <span data-ttu-id="315f7-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="315f7-131">None</span></span>
<span data-ttu-id="315f7-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="315f7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="315f7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="315f7-133">OUTPUTS</span></span>

### <span data-ttu-id="315f7-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="315f7-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="315f7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="315f7-135">NOTES</span></span>

## <span data-ttu-id="315f7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="315f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="315f7-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="315f7-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="315f7-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="315f7-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


