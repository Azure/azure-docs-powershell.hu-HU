---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186234"
---
# <span data-ttu-id="48e32-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="48e32-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="48e32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48e32-102">SYNOPSIS</span></span>
<span data-ttu-id="48e32-103">DSC-bővítmény eltávolítása egy erőforráscsoport virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="48e32-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="48e32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48e32-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e32-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48e32-105">DESCRIPTION</span></span>
<span data-ttu-id="48e32-106">A **Remove-AzVMDscExtension** parancsmag eltávolítja a kívánt állapot-konfigurációs (DSC) bővítményt egy erőforráscsoport virtuális számítógépéről.</span><span class="sxs-lookup"><span data-stu-id="48e32-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="48e32-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48e32-107">EXAMPLES</span></span>

### <span data-ttu-id="48e32-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48e32-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="48e32-109">Ez a parancs eltávolítja a DSC nevű VM07 nevű virtuális gépen a DSC nevű bővítményt.</span><span class="sxs-lookup"><span data-stu-id="48e32-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="48e32-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48e32-110">PARAMETERS</span></span>

### <span data-ttu-id="48e32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e32-111">-DefaultProfile</span></span>
<span data-ttu-id="48e32-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48e32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48e32-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48e32-113">-Name</span></span>
<span data-ttu-id="48e32-114">Annak a DSC-bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="48e32-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="48e32-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Remove-AzVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="48e32-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e32-116">-Várva</span><span class="sxs-lookup"><span data-stu-id="48e32-116">-NoWait</span></span>
<span data-ttu-id="48e32-117">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="48e32-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="48e32-118">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="48e32-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="48e32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e32-119">-ResourceGroupName</span></span>
<span data-ttu-id="48e32-120">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48e32-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="48e32-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="48e32-121">-VMName</span></span>
<span data-ttu-id="48e32-122">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a DSC bővítményt.</span><span class="sxs-lookup"><span data-stu-id="48e32-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e32-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48e32-123">-Confirm</span></span>
<span data-ttu-id="48e32-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48e32-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e32-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e32-125">-WhatIf</span></span>
<span data-ttu-id="48e32-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48e32-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e32-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48e32-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e32-128">CommonParameters</span></span>
<span data-ttu-id="48e32-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48e32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e32-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48e32-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e32-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e32-131">INPUTS</span></span>

### <span data-ttu-id="48e32-132">System. String</span><span class="sxs-lookup"><span data-stu-id="48e32-132">System.String</span></span>

## <span data-ttu-id="48e32-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e32-133">OUTPUTS</span></span>

### <span data-ttu-id="48e32-134">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48e32-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="48e32-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48e32-135">NOTES</span></span>

## <span data-ttu-id="48e32-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48e32-136">RELATED LINKS</span></span>

[<span data-ttu-id="48e32-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="48e32-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="48e32-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="48e32-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)

