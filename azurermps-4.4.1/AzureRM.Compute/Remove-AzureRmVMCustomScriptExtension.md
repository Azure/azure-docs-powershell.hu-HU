---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 2d1edd8e511042f677928f171d7e31859cc5390f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492552"
---
# <span data-ttu-id="08357-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="08357-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="08357-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08357-102">SYNOPSIS</span></span>
<span data-ttu-id="08357-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="08357-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08357-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08357-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08357-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08357-105">DESCRIPTION</span></span>
<span data-ttu-id="08357-106">A **Remove-AzureRmVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="08357-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="08357-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08357-107">EXAMPLES</span></span>

## <span data-ttu-id="08357-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08357-108">PARAMETERS</span></span>

### <span data-ttu-id="08357-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08357-109">-DefaultProfile</span></span>
<span data-ttu-id="08357-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08357-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08357-111">-Force</span><span class="sxs-lookup"><span data-stu-id="08357-111">-Force</span></span>
<span data-ttu-id="08357-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="08357-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08357-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08357-113">-Name</span></span>
<span data-ttu-id="08357-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08357-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08357-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08357-115">-ResourceGroupName</span></span>
<span data-ttu-id="08357-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08357-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="08357-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="08357-117">-VMName</span></span>
<span data-ttu-id="08357-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="08357-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="08357-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08357-119">-Confirm</span></span>
<span data-ttu-id="08357-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08357-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08357-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08357-121">-WhatIf</span></span>
<span data-ttu-id="08357-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08357-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="08357-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08357-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08357-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08357-124">CommonParameters</span></span>
<span data-ttu-id="08357-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08357-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08357-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08357-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08357-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08357-127">INPUTS</span></span>

## <span data-ttu-id="08357-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08357-128">OUTPUTS</span></span>

## <span data-ttu-id="08357-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08357-129">NOTES</span></span>

## <span data-ttu-id="08357-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08357-130">RELATED LINKS</span></span>

[<span data-ttu-id="08357-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="08357-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="08357-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="08357-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
