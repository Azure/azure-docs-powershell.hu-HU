---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850050"
---
# <span data-ttu-id="04154-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="04154-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="04154-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04154-102">SYNOPSIS</span></span>
<span data-ttu-id="04154-103">Eltávolít egy egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="04154-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04154-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04154-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04154-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04154-105">DESCRIPTION</span></span>
<span data-ttu-id="04154-106">A **Remove-AzureRmVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl virtuális gép bővítményét egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="04154-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="04154-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04154-107">EXAMPLES</span></span>

## <span data-ttu-id="04154-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04154-108">PARAMETERS</span></span>

### <span data-ttu-id="04154-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04154-109">-DefaultProfile</span></span>
<span data-ttu-id="04154-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04154-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04154-111">-Force</span><span class="sxs-lookup"><span data-stu-id="04154-111">-Force</span></span>
<span data-ttu-id="04154-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="04154-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04154-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04154-113">-Name</span></span>
<span data-ttu-id="04154-114">A parancsmag által eltávolított egyéni parancsfájl-kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04154-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04154-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04154-115">-ResourceGroupName</span></span>
<span data-ttu-id="04154-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04154-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="04154-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="04154-117">-VMName</span></span>
<span data-ttu-id="04154-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az egyéni parancsfájl-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="04154-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04154-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04154-119">-Confirm</span></span>
<span data-ttu-id="04154-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04154-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04154-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04154-121">-WhatIf</span></span>
<span data-ttu-id="04154-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04154-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="04154-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04154-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04154-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04154-124">CommonParameters</span></span>
<span data-ttu-id="04154-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04154-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04154-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04154-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04154-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04154-127">INPUTS</span></span>

### <span data-ttu-id="04154-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="04154-128">None</span></span>
<span data-ttu-id="04154-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="04154-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04154-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04154-130">OUTPUTS</span></span>

### <span data-ttu-id="04154-131">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04154-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04154-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04154-132">NOTES</span></span>

## <span data-ttu-id="04154-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04154-133">RELATED LINKS</span></span>

[<span data-ttu-id="04154-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="04154-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="04154-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="04154-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
