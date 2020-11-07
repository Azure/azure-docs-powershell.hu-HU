---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 83041e17a930ee63c17f68d6ce8ce2797a25318c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671282"
---
# <span data-ttu-id="667cd-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="667cd-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="667cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="667cd-102">SYNOPSIS</span></span>
<span data-ttu-id="667cd-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="667cd-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="667cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="667cd-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="667cd-105">DESCRIPTION</span></span>
<span data-ttu-id="667cd-106">A **Remove-AzVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="667cd-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="667cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="667cd-107">EXAMPLES</span></span>

## <span data-ttu-id="667cd-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="667cd-108">PARAMETERS</span></span>

### <span data-ttu-id="667cd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667cd-109">-DefaultProfile</span></span>
<span data-ttu-id="667cd-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="667cd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667cd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="667cd-111">-Force</span></span>
<span data-ttu-id="667cd-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="667cd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="667cd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="667cd-113">-Name</span></span>
<span data-ttu-id="667cd-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="667cd-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="667cd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667cd-115">-ResourceGroupName</span></span>
<span data-ttu-id="667cd-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="667cd-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="667cd-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="667cd-117">-VMName</span></span>
<span data-ttu-id="667cd-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="667cd-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="667cd-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="667cd-119">-Confirm</span></span>
<span data-ttu-id="667cd-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="667cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667cd-121">-WhatIf</span></span>
<span data-ttu-id="667cd-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="667cd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667cd-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="667cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667cd-124">CommonParameters</span></span>
<span data-ttu-id="667cd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="667cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667cd-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667cd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="667cd-127">INPUTS</span></span>

### <span data-ttu-id="667cd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="667cd-128">System.String</span></span>

## <span data-ttu-id="667cd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="667cd-129">OUTPUTS</span></span>

### <span data-ttu-id="667cd-130">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="667cd-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="667cd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="667cd-131">NOTES</span></span>

## <span data-ttu-id="667cd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="667cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="667cd-133">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="667cd-133">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="667cd-134">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="667cd-134">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
