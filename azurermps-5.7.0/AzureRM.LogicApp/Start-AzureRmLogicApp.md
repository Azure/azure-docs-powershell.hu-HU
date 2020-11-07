---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680703"
---
# <span data-ttu-id="a2482-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a2482-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="a2482-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2482-102">SYNOPSIS</span></span>
<span data-ttu-id="a2482-103">Egy logikai alkalmazást futtat egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="a2482-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2482-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2482-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2482-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2482-105">DESCRIPTION</span></span>
<span data-ttu-id="a2482-106">A **Start-AzureRmLogicApp** parancsmag a Logic apps funkció segítségével futtatja a logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="a2482-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="a2482-107">Adjon meg egy nevet, erőforráscsoportot és triggert.</span><span class="sxs-lookup"><span data-stu-id="a2482-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="a2482-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a2482-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a2482-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="a2482-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a2482-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="a2482-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a2482-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="a2482-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a2482-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a2482-112">EXAMPLES</span></span>

### <span data-ttu-id="a2482-113">Példa 1: logikai alkalmazás futtatása</span><span class="sxs-lookup"><span data-stu-id="a2482-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="a2482-114">Ez a parancs futtatja a Logic alkalmazást a ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="a2482-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a2482-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2482-115">PARAMETERS</span></span>

### <span data-ttu-id="a2482-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2482-116">-DefaultProfile</span></span>
<span data-ttu-id="a2482-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2482-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2482-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2482-118">-Name</span></span>
<span data-ttu-id="a2482-119">Annak a logikai alkalmazásnak a nevét adja meg, amelyre a parancsmag indul.</span><span class="sxs-lookup"><span data-stu-id="a2482-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2482-120">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="a2482-120">-Parameters</span></span>
<span data-ttu-id="a2482-121">A Logic app Parameters Collection objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2482-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a2482-122">Adjon meg egy kivonatoló táblázatot, szótárt \<string\> vagy szótárat \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="a2482-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2482-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2482-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2482-124">Annak a logikai alkalmazást tartalmazó erőforráscsoportnak a neve, amely a parancsmag kezdetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a2482-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a2482-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a2482-125">-TriggerName</span></span>
<span data-ttu-id="a2482-126">Annak a logikai alkalmazásnak az indítóját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="a2482-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a2482-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2482-127">-Confirm</span></span>
<span data-ttu-id="a2482-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2482-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2482-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2482-129">-WhatIf</span></span>
<span data-ttu-id="a2482-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2482-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2482-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2482-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2482-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2482-132">CommonParameters</span></span>
<span data-ttu-id="a2482-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2482-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2482-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2482-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2482-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2482-135">INPUTS</span></span>

### <span data-ttu-id="a2482-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2482-136">None</span></span>
<span data-ttu-id="a2482-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a2482-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2482-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2482-138">OUTPUTS</span></span>

### <span data-ttu-id="a2482-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a2482-139">System.Object</span></span>

## <span data-ttu-id="a2482-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2482-140">NOTES</span></span>

## <span data-ttu-id="a2482-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2482-141">RELATED LINKS</span></span>

[<span data-ttu-id="a2482-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a2482-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="a2482-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a2482-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="a2482-144">Új – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a2482-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a2482-145">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a2482-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="a2482-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a2482-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a2482-147">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a2482-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


