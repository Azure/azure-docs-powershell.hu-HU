---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 9268d1859f42b7849f8e4a61ae39aa4b68994e4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497407"
---
# <span data-ttu-id="dedf9-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dedf9-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="dedf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dedf9-102">SYNOPSIS</span></span>
<span data-ttu-id="dedf9-103">Egy integrációs fiókpartner eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dedf9-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dedf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dedf9-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dedf9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dedf9-105">DESCRIPTION</span></span>
<span data-ttu-id="dedf9-106">A **Remove-AzureRmIntegrationAccountPartner** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók partnert.</span><span class="sxs-lookup"><span data-stu-id="dedf9-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="dedf9-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="dedf9-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="dedf9-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="dedf9-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dedf9-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="dedf9-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dedf9-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="dedf9-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dedf9-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="dedf9-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dedf9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dedf9-112">EXAMPLES</span></span>

### <span data-ttu-id="dedf9-113">1. példa: az integrációs fiókpartner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dedf9-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="dedf9-114">Ez a parancs eltávolítja a IntegrationAccountPartner1 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="dedf9-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="dedf9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dedf9-115">PARAMETERS</span></span>

### <span data-ttu-id="dedf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedf9-116">-DefaultProfile</span></span>
<span data-ttu-id="dedf9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dedf9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dedf9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dedf9-118">-Force</span></span>
<span data-ttu-id="dedf9-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dedf9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dedf9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dedf9-120">-Name</span></span>
<span data-ttu-id="dedf9-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dedf9-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dedf9-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="dedf9-122">-PartnerName</span></span>
<span data-ttu-id="dedf9-123">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dedf9-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="dedf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="dedf9-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dedf9-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dedf9-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dedf9-126">-Confirm</span></span>
<span data-ttu-id="dedf9-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dedf9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dedf9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dedf9-128">-WhatIf</span></span>
<span data-ttu-id="dedf9-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dedf9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dedf9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dedf9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dedf9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedf9-131">CommonParameters</span></span>
<span data-ttu-id="dedf9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dedf9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedf9-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedf9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedf9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedf9-134">INPUTS</span></span>

### <span data-ttu-id="dedf9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dedf9-135">System.String</span></span>

## <span data-ttu-id="dedf9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedf9-136">OUTPUTS</span></span>

### <span data-ttu-id="dedf9-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="dedf9-137">System.Void</span></span>

## <span data-ttu-id="dedf9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dedf9-138">NOTES</span></span>

## <span data-ttu-id="dedf9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dedf9-139">RELATED LINKS</span></span>

[<span data-ttu-id="dedf9-140">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dedf9-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="dedf9-141">Új – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dedf9-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="dedf9-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dedf9-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


