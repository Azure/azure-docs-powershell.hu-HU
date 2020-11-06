---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495453"
---
# <span data-ttu-id="b856f-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b856f-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="b856f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b856f-102">SYNOPSIS</span></span>
<span data-ttu-id="b856f-103">Információt kap az egyéni parancsfájl-kiterjesztésről.</span><span class="sxs-lookup"><span data-stu-id="b856f-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b856f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b856f-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="b856f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b856f-105">DESCRIPTION</span></span>
<span data-ttu-id="b856f-106">A **Get-AzureRmVMCustomScriptExtension** parancsmag egy virtuális gépen egy egyéni parancsfájl virtuálisgép-bővítményének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b856f-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="b856f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b856f-107">EXAMPLES</span></span>

### <span data-ttu-id="b856f-108">Példa 1: egyéni parancsfájl-kiterjesztés beszerzése</span><span class="sxs-lookup"><span data-stu-id="b856f-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="b856f-109">Ez a parancs a ContosoCustomScript nevű egyéni parancsfájl-kiterjesztést kapja a VirtualMachine07 nevű virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="b856f-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b856f-110">2. példa: egyéni parancsfájl-kiterjesztés példány nézetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="b856f-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="b856f-111">Ez a parancs a VirtualMachine07 nevű virtuális gép ContosoCustomScript nevű egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b856f-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="b856f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b856f-112">PARAMETERS</span></span>

### <span data-ttu-id="b856f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b856f-113">-Name</span></span>
<span data-ttu-id="b856f-114">Annak az egyéni parancsfájlnak a neve, amelyről a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="b856f-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="b856f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b856f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b856f-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b856f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b856f-117">-Állapot</span><span class="sxs-lookup"><span data-stu-id="b856f-117">-Status</span></span>
<span data-ttu-id="b856f-118">Jelzi, hogy ez a parancsmag az egyéni parancsfájl-bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b856f-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="b856f-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b856f-119">-VMName</span></span>
<span data-ttu-id="b856f-120">Annak a virtuális gépnek a neve, amelyhez a parancsmag az egyéni parancsfájl-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="b856f-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="b856f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b856f-121">CommonParameters</span></span>
<span data-ttu-id="b856f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b856f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b856f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b856f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b856f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b856f-124">INPUTS</span></span>

### <span data-ttu-id="b856f-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="b856f-125">None</span></span>
<span data-ttu-id="b856f-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b856f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b856f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b856f-127">OUTPUTS</span></span>

## <span data-ttu-id="b856f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b856f-128">NOTES</span></span>

## <span data-ttu-id="b856f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b856f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b856f-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b856f-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b856f-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b856f-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="b856f-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b856f-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


