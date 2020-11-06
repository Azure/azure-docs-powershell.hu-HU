---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498904"
---
# <span data-ttu-id="83335-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="83335-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="83335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83335-102">SYNOPSIS</span></span>
<span data-ttu-id="83335-103">Egy logikai alkalmazást távolít el egy erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="83335-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83335-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83335-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83335-105">DESCRIPTION</span></span>
<span data-ttu-id="83335-106">A **Remove-AzureRmLogicApp** parancsmag a logikai alkalmazások funkció segítségével távolítja el a logikai alkalmazást egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="83335-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="83335-107">Adja meg a logikai alkalmazást és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="83335-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="83335-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="83335-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="83335-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="83335-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="83335-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="83335-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="83335-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="83335-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="83335-112">Példák</span><span class="sxs-lookup"><span data-stu-id="83335-112">EXAMPLES</span></span>

### <span data-ttu-id="83335-113">1. példa: logikai alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83335-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="83335-114">Ez a parancs eltávolítja a logikai alkalmazást egy erőforráscsoportből.</span><span class="sxs-lookup"><span data-stu-id="83335-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="83335-115">A parancs tartalmazza az *erő* paramétert, amely megakadályozza, hogy a parancs megerősítést kérjen.</span><span class="sxs-lookup"><span data-stu-id="83335-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="83335-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83335-116">PARAMETERS</span></span>

### <span data-ttu-id="83335-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83335-117">-DefaultProfile</span></span>
<span data-ttu-id="83335-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="83335-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83335-119">-Force</span><span class="sxs-lookup"><span data-stu-id="83335-119">-Force</span></span>
<span data-ttu-id="83335-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="83335-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83335-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83335-121">-Name</span></span>
<span data-ttu-id="83335-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="83335-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83335-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83335-123">-ResourceGroupName</span></span>
<span data-ttu-id="83335-124">Annak az erőforráscsoport a nevét adja meg, amely a parancsmag által eltávolított logikai alkalmazást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="83335-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83335-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83335-125">-Confirm</span></span>
<span data-ttu-id="83335-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83335-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83335-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83335-127">-WhatIf</span></span>
<span data-ttu-id="83335-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83335-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83335-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83335-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83335-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83335-130">CommonParameters</span></span>
<span data-ttu-id="83335-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83335-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83335-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83335-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83335-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83335-133">INPUTS</span></span>

### <span data-ttu-id="83335-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="83335-134">None</span></span>
<span data-ttu-id="83335-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="83335-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83335-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83335-136">OUTPUTS</span></span>

### <span data-ttu-id="83335-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="83335-137">System.Object</span></span>

## <span data-ttu-id="83335-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83335-138">NOTES</span></span>

## <span data-ttu-id="83335-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83335-139">RELATED LINKS</span></span>

[<span data-ttu-id="83335-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="83335-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="83335-141">Új – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="83335-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="83335-142">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="83335-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="83335-143">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="83335-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


