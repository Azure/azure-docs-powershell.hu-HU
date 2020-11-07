---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 7342601bba3c963131728f02773cb3b84e917bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835418"
---
# <span data-ttu-id="c7eaa-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c7eaa-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="c7eaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="c7eaa-103">Az integrációs fiók megfeleltetésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-103">Removes an integration account map.</span></span>

## <span data-ttu-id="c7eaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7eaa-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7eaa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="c7eaa-106">A **Remove-AzIntegrationAccountMap** parancsmag egy erőforráscsoport-integrációs fiók megfeleltetését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="c7eaa-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a megfeleltetés nevét.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="c7eaa-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c7eaa-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c7eaa-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c7eaa-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c7eaa-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c7eaa-112">EXAMPLES</span></span>

### <span data-ttu-id="c7eaa-113">1. példa: az integrációs fiók megfeleltetésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c7eaa-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="c7eaa-114">Ez a parancs eltávolítja a IntegrationAccountMap47 nevű integrációs fiók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="c7eaa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7eaa-115">PARAMETERS</span></span>

### <span data-ttu-id="c7eaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7eaa-116">-DefaultProfile</span></span>
<span data-ttu-id="c7eaa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7eaa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7eaa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c7eaa-118">-Force</span></span>
<span data-ttu-id="c7eaa-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7eaa-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="c7eaa-120">-MapName</span></span>
<span data-ttu-id="c7eaa-121">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7eaa-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7eaa-122">-Name</span></span>
<span data-ttu-id="c7eaa-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7eaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7eaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7eaa-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7eaa-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7eaa-126">-Confirm</span></span>
<span data-ttu-id="c7eaa-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7eaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7eaa-128">-WhatIf</span></span>
<span data-ttu-id="c7eaa-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7eaa-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7eaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7eaa-131">CommonParameters</span></span>
<span data-ttu-id="c7eaa-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7eaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7eaa-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7eaa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7eaa-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7eaa-134">INPUTS</span></span>

### <span data-ttu-id="c7eaa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c7eaa-135">System.String</span></span>

## <span data-ttu-id="c7eaa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7eaa-136">OUTPUTS</span></span>

### <span data-ttu-id="c7eaa-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="c7eaa-137">System.Void</span></span>

## <span data-ttu-id="c7eaa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7eaa-138">NOTES</span></span>

## <span data-ttu-id="c7eaa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7eaa-139">RELATED LINKS</span></span>

[<span data-ttu-id="c7eaa-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c7eaa-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="c7eaa-141">Új – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c7eaa-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="c7eaa-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c7eaa-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


