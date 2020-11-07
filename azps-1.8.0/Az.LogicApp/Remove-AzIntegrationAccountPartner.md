---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: d630a88134b2910a38b21ff964db9748db5cbeeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835417"
---
# <span data-ttu-id="36a9f-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="36a9f-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="36a9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="36a9f-103">Egy integrációs fiókpartner eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="36a9f-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="36a9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36a9f-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="36a9f-106">A **Remove-AzIntegrationAccountPartner** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók partnert.</span><span class="sxs-lookup"><span data-stu-id="36a9f-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="36a9f-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="36a9f-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="36a9f-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="36a9f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="36a9f-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="36a9f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="36a9f-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="36a9f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="36a9f-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="36a9f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="36a9f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="36a9f-112">EXAMPLES</span></span>

### <span data-ttu-id="36a9f-113">1. példa: az integrációs fiókpartner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36a9f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="36a9f-114">Ez a parancs eltávolítja a IntegrationAccountPartner1 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="36a9f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="36a9f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36a9f-115">PARAMETERS</span></span>

### <span data-ttu-id="36a9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a9f-116">-DefaultProfile</span></span>
<span data-ttu-id="36a9f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36a9f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a9f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36a9f-118">-Force</span></span>
<span data-ttu-id="36a9f-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="36a9f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36a9f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36a9f-120">-Name</span></span>
<span data-ttu-id="36a9f-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a9f-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="36a9f-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="36a9f-122">-PartnerName</span></span>
<span data-ttu-id="36a9f-123">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a9f-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="36a9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="36a9f-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36a9f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="36a9f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36a9f-126">-Confirm</span></span>
<span data-ttu-id="36a9f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36a9f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a9f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a9f-128">-WhatIf</span></span>
<span data-ttu-id="36a9f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36a9f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a9f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36a9f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a9f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a9f-131">CommonParameters</span></span>
<span data-ttu-id="36a9f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36a9f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a9f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a9f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a9f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a9f-134">INPUTS</span></span>

### <span data-ttu-id="36a9f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="36a9f-135">System.String</span></span>

## <span data-ttu-id="36a9f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a9f-136">OUTPUTS</span></span>

### <span data-ttu-id="36a9f-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="36a9f-137">System.Void</span></span>

## <span data-ttu-id="36a9f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36a9f-138">NOTES</span></span>

## <span data-ttu-id="36a9f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36a9f-139">RELATED LINKS</span></span>

[<span data-ttu-id="36a9f-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="36a9f-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="36a9f-141">Új – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="36a9f-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="36a9f-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="36a9f-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


