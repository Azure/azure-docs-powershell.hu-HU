---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025736"
---
# <span data-ttu-id="ceb7d-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ceb7d-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="ceb7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb7d-103">Eltávolítja a séf kiterjesztését egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="ceb7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceb7d-104">SYNTAX</span></span>

### <span data-ttu-id="ceb7d-105">Linux</span><span class="sxs-lookup"><span data-stu-id="ceb7d-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb7d-106">Windows</span><span class="sxs-lookup"><span data-stu-id="ceb7d-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb7d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceb7d-107">DESCRIPTION</span></span>
<span data-ttu-id="ceb7d-108">A **Remove-AzVMChefExtension** parancsmag eltávolítja a Chef bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="ceb7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ceb7d-109">EXAMPLES</span></span>

### <span data-ttu-id="ceb7d-110">Példa 1: Chef-kiterjesztés eltávolítása Windows Virtual Machine-ből</span><span class="sxs-lookup"><span data-stu-id="ceb7d-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="ceb7d-111">Ez a parancs eltávolítja a Chef bővítményt egy, a WindowsVM001 nevű Windows-beli virtuális gépről, amely a ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="ceb7d-112">2. példa: Chef-kiterjesztés eltávolítása egy linuxos virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="ceb7d-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="ceb7d-113">Ez a parancs eltávolítja a Chef bővítményt egy LinuxVM001 nevű, a ResourceGroup002 nevű erőforráscsoport csoportjába tartozó Linux-beli virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="ceb7d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ceb7d-114">PARAMETERS</span></span>

### <span data-ttu-id="ceb7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb7d-115">-DefaultProfile</span></span>
<span data-ttu-id="ceb7d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceb7d-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="ceb7d-117">-Linux</span></span>
<span data-ttu-id="ceb7d-118">Azt jelzi, hogy ez a parancsmag egy linuxos virtuális gépet céloz meg.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb7d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ceb7d-119">-Name</span></span>
<span data-ttu-id="ceb7d-120">Annak a séf-bővítménynek a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb7d-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="ceb7d-121">-NoWait</span></span>
<span data-ttu-id="ceb7d-122">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ceb7d-123">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ceb7d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb7d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ceb7d-125">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="ceb7d-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="ceb7d-126">-VMName</span></span>
<span data-ttu-id="ceb7d-127">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a szakács bővítményt.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="ceb7d-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="ceb7d-128">-Windows</span></span>
<span data-ttu-id="ceb7d-129">Jelzi, hogy ez a parancsmag a Windows Virtual Machine-t célozza meg.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb7d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ceb7d-130">-Confirm</span></span>
<span data-ttu-id="ceb7d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceb7d-132">-WhatIf</span></span>
<span data-ttu-id="ceb7d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceb7d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb7d-135">CommonParameters</span></span>
<span data-ttu-id="ceb7d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceb7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb7d-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ceb7d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb7d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceb7d-138">INPUTS</span></span>

### <span data-ttu-id="ceb7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ceb7d-139">System.String</span></span>

## <span data-ttu-id="ceb7d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceb7d-140">OUTPUTS</span></span>

### <span data-ttu-id="ceb7d-141">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ceb7d-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ceb7d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceb7d-142">NOTES</span></span>

## <span data-ttu-id="ceb7d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceb7d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ceb7d-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ceb7d-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="ceb7d-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ceb7d-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
