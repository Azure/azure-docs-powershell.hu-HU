---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844369"
---
# <span data-ttu-id="9cf33-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9cf33-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="9cf33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cf33-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf33-103">DSC-bővítmény eltávolítása egy erőforráscsoport virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="9cf33-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="9cf33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cf33-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cf33-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf33-106">A **Remove-AzVMDscExtension** parancsmag eltávolítja a kívánt állapot-konfigurációs (DSC) bővítményt egy erőforráscsoport virtuális számítógépéről.</span><span class="sxs-lookup"><span data-stu-id="9cf33-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="9cf33-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9cf33-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf33-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9cf33-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="9cf33-109">Ez a parancs eltávolítja a DSC nevű VM07 nevű virtuális gépen a DSC nevű bővítményt.</span><span class="sxs-lookup"><span data-stu-id="9cf33-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="9cf33-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cf33-110">PARAMETERS</span></span>

### <span data-ttu-id="9cf33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf33-111">-DefaultProfile</span></span>
<span data-ttu-id="9cf33-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cf33-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf33-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cf33-113">-Name</span></span>
<span data-ttu-id="9cf33-114">Annak a DSC-bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9cf33-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="9cf33-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Remove-AzVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="9cf33-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf33-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf33-116">-ResourceGroupName</span></span>
<span data-ttu-id="9cf33-117">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cf33-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9cf33-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9cf33-118">-VMName</span></span>
<span data-ttu-id="9cf33-119">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a DSC bővítményt.</span><span class="sxs-lookup"><span data-stu-id="9cf33-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf33-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cf33-120">-Confirm</span></span>
<span data-ttu-id="9cf33-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cf33-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf33-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf33-122">-WhatIf</span></span>
<span data-ttu-id="9cf33-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cf33-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9cf33-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cf33-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf33-125">CommonParameters</span></span>
<span data-ttu-id="9cf33-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cf33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf33-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf33-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf33-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cf33-128">INPUTS</span></span>

### <span data-ttu-id="9cf33-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="9cf33-129">None</span></span>
<span data-ttu-id="9cf33-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9cf33-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9cf33-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cf33-131">OUTPUTS</span></span>

### <span data-ttu-id="9cf33-132">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9cf33-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9cf33-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cf33-133">NOTES</span></span>

## <span data-ttu-id="9cf33-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cf33-134">RELATED LINKS</span></span>

[<span data-ttu-id="9cf33-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9cf33-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="9cf33-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9cf33-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


