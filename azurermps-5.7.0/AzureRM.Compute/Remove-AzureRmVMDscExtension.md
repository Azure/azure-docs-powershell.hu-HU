---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b3e9f8703b2130426d98a4a59fe25eb2f3f8fbdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492373"
---
# <span data-ttu-id="79088-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="79088-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="79088-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79088-102">SYNOPSIS</span></span>
<span data-ttu-id="79088-103">DSC-bővítmény eltávolítása egy erőforráscsoport virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="79088-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79088-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79088-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79088-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79088-105">DESCRIPTION</span></span>
<span data-ttu-id="79088-106">A **Remove-AzureRmVMDscExtension** parancsmag eltávolítja a kívánt állapot-konfigurációs (DSC) bővítményt egy erőforráscsoport virtuális számítógépéről.</span><span class="sxs-lookup"><span data-stu-id="79088-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="79088-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79088-107">EXAMPLES</span></span>

### <span data-ttu-id="79088-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="79088-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="79088-109">Ez a parancs eltávolítja a DSC nevű VM07 nevű virtuális gépen a DSC nevű bővítményt.</span><span class="sxs-lookup"><span data-stu-id="79088-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="79088-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79088-110">PARAMETERS</span></span>

### <span data-ttu-id="79088-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79088-111">-Name</span></span>
<span data-ttu-id="79088-112">Annak a DSC-bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="79088-112">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="79088-113">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Remove-AzureRmVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="79088-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="79088-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79088-114">-ResourceGroupName</span></span>
<span data-ttu-id="79088-115">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79088-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="79088-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="79088-116">-VMName</span></span>
<span data-ttu-id="79088-117">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a DSC bővítményt.</span><span class="sxs-lookup"><span data-stu-id="79088-117">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="79088-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79088-118">-Confirm</span></span>
<span data-ttu-id="79088-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79088-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79088-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79088-120">-WhatIf</span></span>
<span data-ttu-id="79088-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79088-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="79088-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79088-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79088-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79088-123">CommonParameters</span></span>
<span data-ttu-id="79088-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79088-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79088-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79088-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79088-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79088-126">INPUTS</span></span>

### <span data-ttu-id="79088-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="79088-127">None</span></span>
<span data-ttu-id="79088-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="79088-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79088-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79088-129">OUTPUTS</span></span>

## <span data-ttu-id="79088-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79088-130">NOTES</span></span>

## <span data-ttu-id="79088-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79088-131">RELATED LINKS</span></span>

[<span data-ttu-id="79088-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="79088-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="79088-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="79088-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


