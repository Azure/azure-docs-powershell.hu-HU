---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495435"
---
# <span data-ttu-id="5ac48-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ac48-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="5ac48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ac48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac48-103">Eltávolítja a séf kiterjesztését egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5ac48-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ac48-104">SYNTAX</span></span>

### <span data-ttu-id="5ac48-105">Linux</span><span class="sxs-lookup"><span data-stu-id="5ac48-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac48-106">Windows</span><span class="sxs-lookup"><span data-stu-id="5ac48-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac48-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ac48-107">DESCRIPTION</span></span>
<span data-ttu-id="5ac48-108">A **Remove-AzureVMChefExtension** parancsmag eltávolítja a Chef bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5ac48-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="5ac48-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5ac48-109">EXAMPLES</span></span>

### <span data-ttu-id="5ac48-110">Példa 1: Chef-kiterjesztés eltávolítása Windows Virtual Machine-ből</span><span class="sxs-lookup"><span data-stu-id="5ac48-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="5ac48-111">Ez a parancs eltávolítja a Chef bővítményt egy, a WindowsVM001 nevű Windows-beli virtuális gépről, amely a ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="5ac48-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="5ac48-112">2. példa: Chef-kiterjesztés eltávolítása egy linuxos virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="5ac48-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="5ac48-113">Ez a parancs eltávolítja a Chef bővítményt egy LinuxVM001 nevű, a ResourceGroup002 nevű erőforráscsoport csoportjába tartozó Linux-beli virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5ac48-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="5ac48-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ac48-114">PARAMETERS</span></span>

### <span data-ttu-id="5ac48-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="5ac48-115">-Linux</span></span>
<span data-ttu-id="5ac48-116">Azt jelzi, hogy ez a parancsmag egy linuxos virtuális gépet céloz meg.</span><span class="sxs-lookup"><span data-stu-id="5ac48-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ac48-117">-Name</span></span>
<span data-ttu-id="5ac48-118">Annak a séf-bővítménynek a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="5ac48-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac48-119">-ResourceGroupName</span></span>
<span data-ttu-id="5ac48-120">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac48-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="5ac48-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="5ac48-121">-VMName</span></span>
<span data-ttu-id="5ac48-122">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a szakács bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5ac48-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="5ac48-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="5ac48-123">-Windows</span></span>
<span data-ttu-id="5ac48-124">Jelzi, hogy ez a parancsmag a Windows Virtual Machine-t célozza meg.</span><span class="sxs-lookup"><span data-stu-id="5ac48-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ac48-125">-Confirm</span></span>
<span data-ttu-id="5ac48-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ac48-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac48-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac48-127">-WhatIf</span></span>
<span data-ttu-id="5ac48-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ac48-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5ac48-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac48-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac48-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac48-130">CommonParameters</span></span>
<span data-ttu-id="5ac48-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ac48-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac48-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac48-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac48-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac48-133">INPUTS</span></span>

### <span data-ttu-id="5ac48-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="5ac48-134">None</span></span>
<span data-ttu-id="5ac48-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5ac48-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ac48-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac48-136">OUTPUTS</span></span>

## <span data-ttu-id="5ac48-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ac48-137">NOTES</span></span>

## <span data-ttu-id="5ac48-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac48-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ac48-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ac48-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="5ac48-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ac48-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
