---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 1fececa1c7d40e8ea2667ecd6461740a6714d744
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667305"
---
# <span data-ttu-id="a1340-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a1340-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="a1340-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1340-102">SYNOPSIS</span></span>
<span data-ttu-id="a1340-103">Eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a1340-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="a1340-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1340-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1340-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1340-105">DESCRIPTION</span></span>
<span data-ttu-id="a1340-106">A **Remove-AzVMAccessExtension** parancsmag eltávolítja a virtuálisgép-hozzáférés (VMAccess) virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="a1340-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="a1340-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1340-107">EXAMPLES</span></span>

## <span data-ttu-id="a1340-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1340-108">PARAMETERS</span></span>

### <span data-ttu-id="a1340-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1340-109">-DefaultProfile</span></span>
<span data-ttu-id="a1340-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1340-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1340-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a1340-111">-Force</span></span>
<span data-ttu-id="a1340-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a1340-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1340-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1340-113">-Name</span></span>
<span data-ttu-id="a1340-114">Itt adhatja meg annak a bővítménynek a nevét, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a1340-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1340-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="a1340-115">-NoWait</span></span>
<span data-ttu-id="a1340-116">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="a1340-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a1340-117">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a1340-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a1340-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1340-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1340-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1340-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a1340-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="a1340-120">-VMName</span></span>
<span data-ttu-id="a1340-121">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1340-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a1340-122">Ez a parancsmag eltávolítja a VMAccess a virtuális gép számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1340-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1340-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1340-123">-Confirm</span></span>
<span data-ttu-id="a1340-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1340-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1340-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1340-125">-WhatIf</span></span>
<span data-ttu-id="a1340-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1340-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1340-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1340-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1340-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1340-128">CommonParameters</span></span>
<span data-ttu-id="a1340-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1340-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1340-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1340-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1340-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1340-131">INPUTS</span></span>

### <span data-ttu-id="a1340-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a1340-132">System.String</span></span>

## <span data-ttu-id="a1340-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1340-133">OUTPUTS</span></span>

### <span data-ttu-id="a1340-134">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a1340-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a1340-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1340-135">NOTES</span></span>

## <span data-ttu-id="a1340-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1340-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1340-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a1340-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="a1340-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a1340-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="a1340-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a1340-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
