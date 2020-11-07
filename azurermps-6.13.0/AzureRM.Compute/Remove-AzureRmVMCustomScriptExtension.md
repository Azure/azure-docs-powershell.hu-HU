---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680391"
---
# <span data-ttu-id="be5e4-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="be5e4-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="be5e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="be5e4-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="be5e4-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be5e4-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="be5e4-106">A **Remove-AzureRmVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="be5e4-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="be5e4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be5e4-107">EXAMPLES</span></span>

## <span data-ttu-id="be5e4-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be5e4-108">PARAMETERS</span></span>

### <span data-ttu-id="be5e4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5e4-109">-DefaultProfile</span></span>
<span data-ttu-id="be5e4-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be5e4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be5e4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="be5e4-111">-Force</span></span>
<span data-ttu-id="be5e4-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="be5e4-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be5e4-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be5e4-113">-Name</span></span>
<span data-ttu-id="be5e4-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be5e4-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be5e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="be5e4-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be5e4-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="be5e4-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="be5e4-117">-VMName</span></span>
<span data-ttu-id="be5e4-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="be5e4-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="be5e4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="be5e4-119">-Confirm</span></span>
<span data-ttu-id="be5e4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be5e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be5e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5e4-121">-WhatIf</span></span>
<span data-ttu-id="be5e4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="be5e4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be5e4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be5e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be5e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5e4-124">CommonParameters</span></span>
<span data-ttu-id="be5e4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be5e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5e4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5e4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5e4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be5e4-127">INPUTS</span></span>

### <span data-ttu-id="be5e4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="be5e4-128">System.String</span></span>

## <span data-ttu-id="be5e4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be5e4-129">OUTPUTS</span></span>

### <span data-ttu-id="be5e4-130">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="be5e4-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="be5e4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be5e4-131">NOTES</span></span>

## <span data-ttu-id="be5e4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be5e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="be5e4-133">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="be5e4-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="be5e4-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="be5e4-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
