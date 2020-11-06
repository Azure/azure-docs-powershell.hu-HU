---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b25b65e9c42cd388d685320802690c6538122e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492834"
---
# <span data-ttu-id="4609a-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4609a-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="4609a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4609a-102">SYNOPSIS</span></span>
<span data-ttu-id="4609a-103">DSC-bővítmény eltávolítása egy erőforráscsoport virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="4609a-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4609a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4609a-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4609a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4609a-105">DESCRIPTION</span></span>
<span data-ttu-id="4609a-106">A **Remove-AzureRmVMDscExtension** parancsmag eltávolítja a kívánt állapot-konfigurációs (DSC) bővítményt egy erőforráscsoport virtuális számítógépéről.</span><span class="sxs-lookup"><span data-stu-id="4609a-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="4609a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4609a-107">EXAMPLES</span></span>

### <span data-ttu-id="4609a-108">1. példa: DSC-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4609a-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="4609a-109">Ez a parancs eltávolítja a DSC nevű VM07 nevű virtuális gépen a DSC nevű bővítményt.</span><span class="sxs-lookup"><span data-stu-id="4609a-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="4609a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4609a-110">PARAMETERS</span></span>

### <span data-ttu-id="4609a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4609a-111">-DefaultProfile</span></span>
<span data-ttu-id="4609a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4609a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4609a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4609a-113">-Name</span></span>
<span data-ttu-id="4609a-114">Annak a DSC-bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4609a-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="4609a-115">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Remove-AzureRmVMDscExtension** által használt alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="4609a-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="4609a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4609a-116">-ResourceGroupName</span></span>
<span data-ttu-id="4609a-117">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4609a-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4609a-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4609a-118">-VMName</span></span>
<span data-ttu-id="4609a-119">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja a DSC bővítményt.</span><span class="sxs-lookup"><span data-stu-id="4609a-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="4609a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4609a-120">-Confirm</span></span>
<span data-ttu-id="4609a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4609a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4609a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4609a-122">-WhatIf</span></span>
<span data-ttu-id="4609a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4609a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4609a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4609a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4609a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4609a-125">CommonParameters</span></span>
<span data-ttu-id="4609a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4609a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4609a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4609a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4609a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4609a-128">INPUTS</span></span>

### <span data-ttu-id="4609a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4609a-129">System.String</span></span>

## <span data-ttu-id="4609a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4609a-130">OUTPUTS</span></span>

### <span data-ttu-id="4609a-131">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4609a-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4609a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4609a-132">NOTES</span></span>

## <span data-ttu-id="4609a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4609a-133">RELATED LINKS</span></span>

[<span data-ttu-id="4609a-134">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4609a-134">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="4609a-135">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4609a-135">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


