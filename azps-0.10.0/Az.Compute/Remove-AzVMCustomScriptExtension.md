---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844386"
---
# <span data-ttu-id="a8b17-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a8b17-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="a8b17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8b17-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b17-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a8b17-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="a8b17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8b17-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b17-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8b17-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b17-106">A **Remove-AzVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a8b17-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="a8b17-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8b17-107">EXAMPLES</span></span>

## <span data-ttu-id="a8b17-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8b17-108">PARAMETERS</span></span>

### <span data-ttu-id="a8b17-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b17-109">-DefaultProfile</span></span>
<span data-ttu-id="a8b17-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8b17-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8b17-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a8b17-111">-Force</span></span>
<span data-ttu-id="a8b17-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a8b17-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8b17-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8b17-113">-Name</span></span>
<span data-ttu-id="a8b17-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8b17-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8b17-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b17-115">-ResourceGroupName</span></span>
<span data-ttu-id="a8b17-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8b17-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a8b17-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a8b17-117">-VMName</span></span>
<span data-ttu-id="a8b17-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a8b17-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="a8b17-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8b17-119">-Confirm</span></span>
<span data-ttu-id="a8b17-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8b17-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b17-121">-WhatIf</span></span>
<span data-ttu-id="a8b17-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8b17-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a8b17-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8b17-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b17-124">CommonParameters</span></span>
<span data-ttu-id="a8b17-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8b17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b17-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b17-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b17-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8b17-127">INPUTS</span></span>

### <span data-ttu-id="a8b17-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8b17-128">None</span></span>
<span data-ttu-id="a8b17-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a8b17-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8b17-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8b17-130">OUTPUTS</span></span>

### <span data-ttu-id="a8b17-131">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a8b17-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a8b17-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8b17-132">NOTES</span></span>

## <span data-ttu-id="a8b17-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8b17-133">RELATED LINKS</span></span>

[<span data-ttu-id="a8b17-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a8b17-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="a8b17-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a8b17-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
