---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 0925b526fa70718fbd648668f80af98882382f57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667291"
---
# <span data-ttu-id="1da6e-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1da6e-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="1da6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1da6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1da6e-103">Eltávolít egy virtuális gépről a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="1da6e-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="1da6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1da6e-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1da6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1da6e-105">DESCRIPTION</span></span>
<span data-ttu-id="1da6e-106">A **Remove-AzVMExtension** parancsmag eltávolítja a virtuális gép virtuálisgép-bővítményeinek bővítményét.</span><span class="sxs-lookup"><span data-stu-id="1da6e-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="1da6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1da6e-107">EXAMPLES</span></span>

### <span data-ttu-id="1da6e-108">1. példa: bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="1da6e-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="1da6e-109">Ez a parancs eltávolítja a ContosoTest nevű bővítményt a ResourceGroup11 nevű VirtualMachine22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="1da6e-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="1da6e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1da6e-110">PARAMETERS</span></span>

### <span data-ttu-id="1da6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da6e-111">-DefaultProfile</span></span>
<span data-ttu-id="1da6e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1da6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da6e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1da6e-113">-Force</span></span>
<span data-ttu-id="1da6e-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1da6e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1da6e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1da6e-115">-Name</span></span>
<span data-ttu-id="1da6e-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1da6e-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1da6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1da6e-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1da6e-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1da6e-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1da6e-119">-VMName</span></span>
<span data-ttu-id="1da6e-120">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="1da6e-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="1da6e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1da6e-121">-Confirm</span></span>
<span data-ttu-id="1da6e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1da6e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1da6e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1da6e-123">-WhatIf</span></span>
<span data-ttu-id="1da6e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1da6e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1da6e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1da6e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1da6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da6e-126">CommonParameters</span></span>
<span data-ttu-id="1da6e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1da6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da6e-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1da6e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da6e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1da6e-129">INPUTS</span></span>

### <span data-ttu-id="1da6e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1da6e-130">System.String</span></span>

## <span data-ttu-id="1da6e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1da6e-131">OUTPUTS</span></span>

### <span data-ttu-id="1da6e-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1da6e-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1da6e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1da6e-133">NOTES</span></span>

## <span data-ttu-id="1da6e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1da6e-134">RELATED LINKS</span></span>

[<span data-ttu-id="1da6e-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1da6e-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="1da6e-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1da6e-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


