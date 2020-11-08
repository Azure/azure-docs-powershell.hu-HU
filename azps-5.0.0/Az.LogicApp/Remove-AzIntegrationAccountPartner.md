---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194669"
---
# <span data-ttu-id="0a313-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0a313-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="0a313-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a313-102">SYNOPSIS</span></span>
<span data-ttu-id="0a313-103">Egy integrációs fiókpartner eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a313-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="0a313-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a313-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a313-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a313-105">DESCRIPTION</span></span>
<span data-ttu-id="0a313-106">A **Remove-AzIntegrationAccountPartner** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók partnert.</span><span class="sxs-lookup"><span data-stu-id="0a313-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="0a313-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="0a313-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="0a313-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0a313-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0a313-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0a313-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0a313-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="0a313-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a313-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="0a313-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a313-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0a313-112">EXAMPLES</span></span>

### <span data-ttu-id="0a313-113">1. példa: az integrációs fiókpartner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a313-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="0a313-114">Ez a parancs eltávolítja a IntegrationAccountPartner1 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="0a313-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="0a313-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a313-115">PARAMETERS</span></span>

### <span data-ttu-id="0a313-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a313-116">-DefaultProfile</span></span>
<span data-ttu-id="0a313-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a313-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a313-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0a313-118">-Force</span></span>
<span data-ttu-id="0a313-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0a313-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a313-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a313-120">-Name</span></span>
<span data-ttu-id="0a313-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a313-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="0a313-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="0a313-122">-PartnerName</span></span>
<span data-ttu-id="0a313-123">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a313-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="0a313-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a313-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a313-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a313-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0a313-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a313-126">-Confirm</span></span>
<span data-ttu-id="0a313-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a313-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a313-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a313-128">-WhatIf</span></span>
<span data-ttu-id="0a313-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a313-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a313-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a313-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a313-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a313-131">CommonParameters</span></span>
<span data-ttu-id="0a313-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a313-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a313-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a313-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a313-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a313-134">INPUTS</span></span>

### <span data-ttu-id="0a313-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0a313-135">System.String</span></span>

## <span data-ttu-id="0a313-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a313-136">OUTPUTS</span></span>

### <span data-ttu-id="0a313-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="0a313-137">System.Void</span></span>

## <span data-ttu-id="0a313-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a313-138">NOTES</span></span>

## <span data-ttu-id="0a313-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a313-139">RELATED LINKS</span></span>

[<span data-ttu-id="0a313-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0a313-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="0a313-141">Új – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0a313-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="0a313-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0a313-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

