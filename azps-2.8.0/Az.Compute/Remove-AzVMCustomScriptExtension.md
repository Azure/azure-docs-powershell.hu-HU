---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667298"
---
# <span data-ttu-id="8816c-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8816c-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="8816c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8816c-102">SYNOPSIS</span></span>
<span data-ttu-id="8816c-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="8816c-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="8816c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8816c-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8816c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8816c-105">DESCRIPTION</span></span>
<span data-ttu-id="8816c-106">A **Remove-AzVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="8816c-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8816c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8816c-107">EXAMPLES</span></span>

## <span data-ttu-id="8816c-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8816c-108">PARAMETERS</span></span>

### <span data-ttu-id="8816c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8816c-109">-DefaultProfile</span></span>
<span data-ttu-id="8816c-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8816c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8816c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8816c-111">-Force</span></span>
<span data-ttu-id="8816c-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8816c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8816c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8816c-113">-Name</span></span>
<span data-ttu-id="8816c-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8816c-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8816c-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="8816c-115">-NoWait</span></span>
<span data-ttu-id="8816c-116">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="8816c-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8816c-117">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="8816c-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8816c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8816c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8816c-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8816c-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8816c-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="8816c-120">-VMName</span></span>
<span data-ttu-id="8816c-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8816c-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="8816c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8816c-122">-Confirm</span></span>
<span data-ttu-id="8816c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8816c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8816c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8816c-124">-WhatIf</span></span>
<span data-ttu-id="8816c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8816c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8816c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8816c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8816c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8816c-127">CommonParameters</span></span>
<span data-ttu-id="8816c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8816c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8816c-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8816c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8816c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8816c-130">INPUTS</span></span>

### <span data-ttu-id="8816c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8816c-131">System.String</span></span>

## <span data-ttu-id="8816c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8816c-132">OUTPUTS</span></span>

### <span data-ttu-id="8816c-133">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8816c-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8816c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8816c-134">NOTES</span></span>

## <span data-ttu-id="8816c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8816c-135">RELATED LINKS</span></span>

[<span data-ttu-id="8816c-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8816c-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="8816c-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8816c-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
