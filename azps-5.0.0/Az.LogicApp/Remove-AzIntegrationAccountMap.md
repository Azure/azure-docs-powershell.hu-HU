---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194673"
---
# <span data-ttu-id="7ca69-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ca69-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="7ca69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ca69-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca69-103">Az integrációs fiók megfeleltetésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7ca69-103">Removes an integration account map.</span></span>

## <span data-ttu-id="7ca69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ca69-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ca69-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca69-106">A **Remove-AzIntegrationAccountMap** parancsmag egy erőforráscsoport-integrációs fiók megfeleltetését távolítja el.</span><span class="sxs-lookup"><span data-stu-id="7ca69-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="7ca69-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a megfeleltetés nevét.</span><span class="sxs-lookup"><span data-stu-id="7ca69-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="7ca69-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7ca69-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7ca69-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7ca69-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7ca69-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7ca69-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7ca69-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7ca69-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7ca69-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7ca69-112">EXAMPLES</span></span>

### <span data-ttu-id="7ca69-113">1. példa: az integrációs fiók megfeleltetésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7ca69-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="7ca69-114">Ez a parancs eltávolítja a IntegrationAccountMap47 nevű integrációs fiók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="7ca69-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="7ca69-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ca69-115">PARAMETERS</span></span>

### <span data-ttu-id="7ca69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca69-116">-DefaultProfile</span></span>
<span data-ttu-id="7ca69-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ca69-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ca69-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7ca69-118">-Force</span></span>
<span data-ttu-id="7ca69-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7ca69-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ca69-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="7ca69-120">-MapName</span></span>
<span data-ttu-id="7ca69-121">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca69-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="7ca69-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ca69-122">-Name</span></span>
<span data-ttu-id="7ca69-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca69-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="7ca69-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca69-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ca69-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca69-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7ca69-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ca69-126">-Confirm</span></span>
<span data-ttu-id="7ca69-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ca69-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca69-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca69-128">-WhatIf</span></span>
<span data-ttu-id="7ca69-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ca69-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca69-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ca69-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca69-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca69-131">CommonParameters</span></span>
<span data-ttu-id="7ca69-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ca69-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca69-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca69-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca69-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca69-134">INPUTS</span></span>

### <span data-ttu-id="7ca69-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca69-135">System.String</span></span>

## <span data-ttu-id="7ca69-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca69-136">OUTPUTS</span></span>

### <span data-ttu-id="7ca69-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="7ca69-137">System.Void</span></span>

## <span data-ttu-id="7ca69-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ca69-138">NOTES</span></span>

## <span data-ttu-id="7ca69-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ca69-139">RELATED LINKS</span></span>

[<span data-ttu-id="7ca69-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ca69-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="7ca69-141">Új – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ca69-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="7ca69-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ca69-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


