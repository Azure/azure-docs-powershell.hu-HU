---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: cd269c015870ab2a030ee44ebfd0f01874b674f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497399"
---
# <span data-ttu-id="8fd2d-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8fd2d-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="8fd2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fd2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd2d-103">Egy logikai alkalmazás futtatásának lemondása</span><span class="sxs-lookup"><span data-stu-id="8fd2d-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fd2d-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fd2d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd2d-106">A **stop-AzureRmLogicAppRun** parancsmag megszünteti a logikai alkalmazások futtatását.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="8fd2d-107">Adja meg a logikai alkalmazást, az erőforrás csoportot és a futtatást.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="8fd2d-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8fd2d-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8fd2d-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8fd2d-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8fd2d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8fd2d-112">EXAMPLES</span></span>

### <span data-ttu-id="8fd2d-113">1. példa: egy logikai alkalmazás futtatásának lemondása</span><span class="sxs-lookup"><span data-stu-id="8fd2d-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzureRmLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="8fd2d-114">Ez a parancs lemondja a LogicApp03 nevű logikai app futtatását.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="8fd2d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fd2d-115">PARAMETERS</span></span>

### <span data-ttu-id="8fd2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd2d-116">-DefaultProfile</span></span>
<span data-ttu-id="8fd2d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fd2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fd2d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8fd2d-118">-Force</span></span>
<span data-ttu-id="8fd2d-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fd2d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fd2d-120">-Name</span></span>
<span data-ttu-id="8fd2d-121">Annak a logikai alkalmazásnak a neve, amelyhez ez a parancsmag lemondja a futást.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fd2d-123">Annak a csoportnak a nevét adja meg, amelyben a parancsmag lemondja a futást.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="8fd2d-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="8fd2d-124">-RunName</span></span>
<span data-ttu-id="8fd2d-125">Annak a logikai alkalmazásnak a nevét adja meg, amelyet a parancsmag lemond.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="8fd2d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8fd2d-126">-Confirm</span></span>
<span data-ttu-id="8fd2d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd2d-128">-WhatIf</span></span>
<span data-ttu-id="8fd2d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd2d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fd2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd2d-131">CommonParameters</span></span>
<span data-ttu-id="8fd2d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fd2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd2d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd2d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd2d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd2d-134">INPUTS</span></span>

### <span data-ttu-id="8fd2d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd2d-135">System.String</span></span>

## <span data-ttu-id="8fd2d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd2d-136">OUTPUTS</span></span>

### <span data-ttu-id="8fd2d-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="8fd2d-137">System.Void</span></span>

## <span data-ttu-id="8fd2d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fd2d-138">NOTES</span></span>

## <span data-ttu-id="8fd2d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fd2d-139">RELATED LINKS</span></span>

[<span data-ttu-id="8fd2d-140">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8fd2d-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


