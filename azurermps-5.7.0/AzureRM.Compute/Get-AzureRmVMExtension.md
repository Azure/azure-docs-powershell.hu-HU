---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493206"
---
# <span data-ttu-id="3700c-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3700c-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="3700c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3700c-102">SYNOPSIS</span></span>
<span data-ttu-id="3700c-103">A virtuálisgép-bővítmények tulajdonságait a virtuális gépen telepítette.</span><span class="sxs-lookup"><span data-stu-id="3700c-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3700c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3700c-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="3700c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3700c-105">DESCRIPTION</span></span>
<span data-ttu-id="3700c-106">A **Get-AzureRmVMExtension** parancsmag a virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="3700c-107">Adja meg annak a bővítménynek a nevét, amelyhez tulajdonságokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="3700c-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="3700c-108">Ha csak a bővítmény példány nézetét szeretné látni, adja meg az állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="3700c-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="3700c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3700c-109">EXAMPLES</span></span>

### <span data-ttu-id="3700c-110">Példa 1: bővítmény tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="3700c-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="3700c-111">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait az erőforráscsoport ResourceGroup11 VirtualMachine22 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="3700c-112">2. példa: egy bővítmény példány nézetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="3700c-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="3700c-113">Ez a parancs a CustomScriptExtension nevű VirtualMachine22 nevű virtuális gép példány nézetét kapja meg az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3700c-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3700c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3700c-114">PARAMETERS</span></span>

### <span data-ttu-id="3700c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3700c-115">-Name</span></span>
<span data-ttu-id="3700c-116">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="3700c-117">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="3700c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3700c-118">-ResourceGroupName</span></span>
<span data-ttu-id="3700c-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3700c-120">-Állapot</span><span class="sxs-lookup"><span data-stu-id="3700c-120">-Status</span></span>
<span data-ttu-id="3700c-121">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="3700c-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="3700c-122">-VMName</span></span>
<span data-ttu-id="3700c-123">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3700c-124">Ez a parancsmag a virtuális gép egy bővítményének tulajdonságait adja meg, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3700c-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3700c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3700c-125">CommonParameters</span></span>
<span data-ttu-id="3700c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3700c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3700c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3700c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3700c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3700c-128">INPUTS</span></span>

### <span data-ttu-id="3700c-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="3700c-129">None</span></span>
<span data-ttu-id="3700c-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3700c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3700c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3700c-131">OUTPUTS</span></span>

## <span data-ttu-id="3700c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3700c-132">NOTES</span></span>

## <span data-ttu-id="3700c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3700c-133">RELATED LINKS</span></span>

[<span data-ttu-id="3700c-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3700c-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="3700c-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3700c-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


