---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495432"
---
# <span data-ttu-id="aa014-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa014-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="aa014-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa014-102">SYNOPSIS</span></span>
<span data-ttu-id="aa014-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="aa014-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa014-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa014-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa014-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa014-105">DESCRIPTION</span></span>
<span data-ttu-id="aa014-106">A **Remove-AzureRmVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="aa014-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="aa014-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa014-107">EXAMPLES</span></span>

## <span data-ttu-id="aa014-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa014-108">PARAMETERS</span></span>

### <span data-ttu-id="aa014-109">-Force</span><span class="sxs-lookup"><span data-stu-id="aa014-109">-Force</span></span>
<span data-ttu-id="aa014-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="aa014-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa014-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa014-111">-Name</span></span>
<span data-ttu-id="aa014-112">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa014-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa014-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa014-113">-ResourceGroupName</span></span>
<span data-ttu-id="aa014-114">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa014-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aa014-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa014-115">-VMName</span></span>
<span data-ttu-id="aa014-116">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aa014-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="aa014-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa014-117">-Confirm</span></span>
<span data-ttu-id="aa014-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa014-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa014-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa014-119">-WhatIf</span></span>
<span data-ttu-id="aa014-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa014-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="aa014-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa014-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa014-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa014-122">CommonParameters</span></span>
<span data-ttu-id="aa014-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa014-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa014-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa014-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa014-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa014-125">INPUTS</span></span>

### <span data-ttu-id="aa014-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="aa014-126">None</span></span>
<span data-ttu-id="aa014-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="aa014-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa014-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa014-128">OUTPUTS</span></span>

## <span data-ttu-id="aa014-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa014-129">NOTES</span></span>

## <span data-ttu-id="aa014-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa014-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa014-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa014-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="aa014-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa014-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
