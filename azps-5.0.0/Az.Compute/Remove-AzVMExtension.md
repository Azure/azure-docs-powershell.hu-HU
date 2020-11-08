---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194111"
---
# <span data-ttu-id="9eef9-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9eef9-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="9eef9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9eef9-102">SYNOPSIS</span></span>
<span data-ttu-id="9eef9-103">Eltávolít egy virtuális gépről a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="9eef9-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="9eef9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9eef9-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eef9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9eef9-105">DESCRIPTION</span></span>
<span data-ttu-id="9eef9-106">A **Remove-AzVMExtension** parancsmag eltávolítja a virtuális gép virtuálisgép-bővítményeinek bővítményét.</span><span class="sxs-lookup"><span data-stu-id="9eef9-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="9eef9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9eef9-107">EXAMPLES</span></span>

### <span data-ttu-id="9eef9-108">1. példa: bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="9eef9-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="9eef9-109">Ez a parancs eltávolítja a ContosoTest nevű bővítményt a ResourceGroup11 nevű VirtualMachine22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="9eef9-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="9eef9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9eef9-110">PARAMETERS</span></span>

### <span data-ttu-id="9eef9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eef9-111">-DefaultProfile</span></span>
<span data-ttu-id="9eef9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eef9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eef9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9eef9-113">-Force</span></span>
<span data-ttu-id="9eef9-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9eef9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9eef9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9eef9-115">-Name</span></span>
<span data-ttu-id="9eef9-116">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9eef9-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9eef9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eef9-117">-ResourceGroupName</span></span>
<span data-ttu-id="9eef9-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9eef9-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9eef9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="9eef9-119">-VMName</span></span>
<span data-ttu-id="9eef9-120">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="9eef9-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="9eef9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9eef9-121">-Confirm</span></span>
<span data-ttu-id="9eef9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9eef9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eef9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eef9-123">-WhatIf</span></span>
<span data-ttu-id="9eef9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9eef9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eef9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9eef9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eef9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eef9-126">CommonParameters</span></span>
<span data-ttu-id="9eef9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9eef9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eef9-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9eef9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eef9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eef9-129">INPUTS</span></span>

### <span data-ttu-id="9eef9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9eef9-130">System.String</span></span>

## <span data-ttu-id="9eef9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eef9-131">OUTPUTS</span></span>

### <span data-ttu-id="9eef9-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9eef9-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9eef9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9eef9-133">NOTES</span></span>

## <span data-ttu-id="9eef9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eef9-134">RELATED LINKS</span></span>

[<span data-ttu-id="9eef9-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9eef9-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="9eef9-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9eef9-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


