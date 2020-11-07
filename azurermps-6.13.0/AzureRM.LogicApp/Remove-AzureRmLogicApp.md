---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 46515fc76d246ffdb4207afb0300613b52cae0a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680082"
---
# <span data-ttu-id="6ff2c-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ff2c-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="6ff2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ff2c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff2c-103">Egy logikai alkalmazást távolít el egy erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ff2c-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ff2c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff2c-106">A **Remove-AzureRmLogicApp** parancsmag a logikai alkalmazások funkció segítségével távolítja el a logikai alkalmazást egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="6ff2c-107">Adja meg a logikai alkalmazást és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6ff2c-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6ff2c-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6ff2c-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6ff2c-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6ff2c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6ff2c-112">EXAMPLES</span></span>

### <span data-ttu-id="6ff2c-113">1. példa: logikai alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6ff2c-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="6ff2c-114">Ez a parancs eltávolítja a logikai alkalmazást egy erőforráscsoportből.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="6ff2c-115">A parancs tartalmazza az *erő* paramétert, amely megakadályozza, hogy a parancs megerősítést kérjen.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="6ff2c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ff2c-116">PARAMETERS</span></span>

### <span data-ttu-id="6ff2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff2c-117">-DefaultProfile</span></span>
<span data-ttu-id="6ff2c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6ff2c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ff2c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6ff2c-119">-Force</span></span>
<span data-ttu-id="6ff2c-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ff2c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ff2c-121">-Name</span></span>
<span data-ttu-id="6ff2c-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6ff2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ff2c-124">Annak az erőforráscsoport a nevét adja meg, amely a parancsmag által eltávolított logikai alkalmazást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6ff2c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ff2c-125">-Confirm</span></span>
<span data-ttu-id="6ff2c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff2c-127">-WhatIf</span></span>
<span data-ttu-id="6ff2c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff2c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ff2c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff2c-130">CommonParameters</span></span>
<span data-ttu-id="6ff2c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ff2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff2c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff2c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff2c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff2c-133">INPUTS</span></span>

### <span data-ttu-id="6ff2c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff2c-134">System.String</span></span>

## <span data-ttu-id="6ff2c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff2c-135">OUTPUTS</span></span>

### <span data-ttu-id="6ff2c-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="6ff2c-136">System.Void</span></span>

## <span data-ttu-id="6ff2c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ff2c-137">NOTES</span></span>

## <span data-ttu-id="6ff2c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ff2c-139">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ff2c-139">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="6ff2c-140">Új – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ff2c-140">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="6ff2c-141">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ff2c-141">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="6ff2c-142">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6ff2c-142">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


