---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 4aaee403007561797614b2534e29c5918dad3643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501160"
---
# <span data-ttu-id="126c4-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="126c4-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="126c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="126c4-102">SYNOPSIS</span></span>
<span data-ttu-id="126c4-103">A virtuálisgép-bővítmények tulajdonságait a virtuális gépen telepítette.</span><span class="sxs-lookup"><span data-stu-id="126c4-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="126c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="126c4-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="126c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="126c4-105">DESCRIPTION</span></span>
<span data-ttu-id="126c4-106">A **Get-AzureRmVMExtension** parancsmag a virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="126c4-107">Adja meg annak a bővítménynek a nevét, amelyhez tulajdonságokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="126c4-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="126c4-108">Ha csak a bővítmény példány nézetét szeretné látni, adja meg az állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="126c4-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="126c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="126c4-109">EXAMPLES</span></span>

### <span data-ttu-id="126c4-110">Példa 1: bővítmény tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="126c4-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="126c4-111">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait az erőforráscsoport ResourceGroup11 VirtualMachine22 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="126c4-112">2. példa: egy bővítmény példány nézetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="126c4-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="126c4-113">Ez a parancs a CustomScriptExtension nevű VirtualMachine22 nevű virtuális gép példány nézetét kapja meg az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="126c4-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="126c4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="126c4-114">PARAMETERS</span></span>

### <span data-ttu-id="126c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126c4-115">-DefaultProfile</span></span>
<span data-ttu-id="126c4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="126c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="126c4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="126c4-117">-Name</span></span>
<span data-ttu-id="126c4-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="126c4-119">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="126c4-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-122">-Állapot</span><span class="sxs-lookup"><span data-stu-id="126c4-122">-Status</span></span>
<span data-ttu-id="126c4-123">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="126c4-124">-VMName</span></span>
<span data-ttu-id="126c4-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="126c4-126">Ez a parancsmag a virtuális gép egy bővítményének tulajdonságait adja meg, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="126c4-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126c4-127">CommonParameters</span></span>
<span data-ttu-id="126c4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="126c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126c4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126c4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="126c4-130">INPUTS</span></span>

### <span data-ttu-id="126c4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="126c4-131">System.String</span></span>

### <span data-ttu-id="126c4-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="126c4-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="126c4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="126c4-133">OUTPUTS</span></span>

### <span data-ttu-id="126c4-134">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="126c4-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="126c4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="126c4-135">NOTES</span></span>

## <span data-ttu-id="126c4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="126c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="126c4-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="126c4-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="126c4-138">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="126c4-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


