---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492370"
---
# <span data-ttu-id="8483e-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8483e-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="8483e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8483e-102">SYNOPSIS</span></span>
<span data-ttu-id="8483e-103">Eltávolít egy virtuális gépről a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8483e-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8483e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8483e-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8483e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8483e-105">DESCRIPTION</span></span>
<span data-ttu-id="8483e-106">A **Remove-AzureRmVMExtension** parancsmag eltávolítja a virtuális gép virtuálisgép-bővítményeinek bővítményét.</span><span class="sxs-lookup"><span data-stu-id="8483e-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="8483e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8483e-107">EXAMPLES</span></span>

### <span data-ttu-id="8483e-108">1. példa: bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="8483e-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="8483e-109">Ez a parancs eltávolítja a ContosoTest nevű bővítményt a ResourceGroup11 nevű VirtualMachine22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="8483e-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="8483e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8483e-110">PARAMETERS</span></span>

### <span data-ttu-id="8483e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8483e-111">-Force</span></span>
<span data-ttu-id="8483e-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8483e-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8483e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8483e-113">-Name</span></span>
<span data-ttu-id="8483e-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8483e-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8483e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8483e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8483e-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8483e-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8483e-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8483e-117">-VMName</span></span>
<span data-ttu-id="8483e-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8483e-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="8483e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8483e-119">-Confirm</span></span>
<span data-ttu-id="8483e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8483e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8483e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8483e-121">-WhatIf</span></span>
<span data-ttu-id="8483e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8483e-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8483e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8483e-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8483e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8483e-124">CommonParameters</span></span>
<span data-ttu-id="8483e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8483e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8483e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8483e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8483e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8483e-127">INPUTS</span></span>

### <span data-ttu-id="8483e-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="8483e-128">None</span></span>
<span data-ttu-id="8483e-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8483e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8483e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8483e-130">OUTPUTS</span></span>

## <span data-ttu-id="8483e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8483e-131">NOTES</span></span>

## <span data-ttu-id="8483e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8483e-132">RELATED LINKS</span></span>

[<span data-ttu-id="8483e-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8483e-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="8483e-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8483e-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


