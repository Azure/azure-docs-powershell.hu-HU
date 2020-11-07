---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 3458eef92b18ea5407724a2ad1b0cb2e10024233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666019"
---
# <span data-ttu-id="acf0e-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="acf0e-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="acf0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="acf0e-103">Egy logikai alkalmazást távolít el egy erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="acf0e-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="acf0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acf0e-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="acf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="acf0e-106">A **Remove-AzLogicApp** parancsmag a logikai alkalmazások funkció segítségével távolítja el a logikai alkalmazást egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="acf0e-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="acf0e-107">Adja meg a logikai alkalmazást és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="acf0e-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="acf0e-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="acf0e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="acf0e-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="acf0e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="acf0e-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="acf0e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="acf0e-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="acf0e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="acf0e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="acf0e-112">EXAMPLES</span></span>

### <span data-ttu-id="acf0e-113">1. példa: logikai alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="acf0e-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="acf0e-114">Ez a parancs eltávolítja a logikai alkalmazást egy erőforráscsoportből.</span><span class="sxs-lookup"><span data-stu-id="acf0e-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="acf0e-115">A parancs tartalmazza az *erő* paramétert, amely megakadályozza, hogy a parancs megerősítést kérjen.</span><span class="sxs-lookup"><span data-stu-id="acf0e-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="acf0e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acf0e-116">PARAMETERS</span></span>

### <span data-ttu-id="acf0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf0e-117">-DefaultProfile</span></span>
<span data-ttu-id="acf0e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="acf0e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acf0e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="acf0e-119">-Force</span></span>
<span data-ttu-id="acf0e-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="acf0e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="acf0e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acf0e-121">-Name</span></span>
<span data-ttu-id="acf0e-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="acf0e-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf0e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf0e-123">-ResourceGroupName</span></span>
<span data-ttu-id="acf0e-124">Annak az erőforráscsoport a nevét adja meg, amely a parancsmag által eltávolított logikai alkalmazást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="acf0e-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf0e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="acf0e-125">-Confirm</span></span>
<span data-ttu-id="acf0e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="acf0e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf0e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf0e-127">-WhatIf</span></span>
<span data-ttu-id="acf0e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="acf0e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf0e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="acf0e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf0e-130">CommonParameters</span></span>
<span data-ttu-id="acf0e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acf0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf0e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf0e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf0e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf0e-133">INPUTS</span></span>

### <span data-ttu-id="acf0e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="acf0e-134">System.String</span></span>

## <span data-ttu-id="acf0e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acf0e-135">OUTPUTS</span></span>

### <span data-ttu-id="acf0e-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="acf0e-136">System.Void</span></span>

## <span data-ttu-id="acf0e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acf0e-137">NOTES</span></span>

## <span data-ttu-id="acf0e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acf0e-138">RELATED LINKS</span></span>

[<span data-ttu-id="acf0e-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="acf0e-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="acf0e-140">Új – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="acf0e-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="acf0e-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="acf0e-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="acf0e-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="acf0e-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


