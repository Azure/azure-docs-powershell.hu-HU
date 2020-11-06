---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: f10173dce7b64ccc656e2c852c6eb20230d1a7bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501796"
---
# <span data-ttu-id="265f4-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="265f4-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="265f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="265f4-102">SYNOPSIS</span></span>
<span data-ttu-id="265f4-103">Egy integrációs fiókpartner eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="265f4-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="265f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="265f4-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="265f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="265f4-105">DESCRIPTION</span></span>
<span data-ttu-id="265f4-106">A **Remove-AzureRmIntegrationAccountPartner** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók partnert.</span><span class="sxs-lookup"><span data-stu-id="265f4-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="265f4-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="265f4-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="265f4-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="265f4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="265f4-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="265f4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="265f4-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="265f4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="265f4-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="265f4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="265f4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="265f4-112">EXAMPLES</span></span>

### <span data-ttu-id="265f4-113">1. példa: az integrációs fiókpartner eltávolítása</span><span class="sxs-lookup"><span data-stu-id="265f4-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="265f4-114">Ez a parancs eltávolítja a IntegrationAccountPartner1 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="265f4-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="265f4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="265f4-115">PARAMETERS</span></span>

### <span data-ttu-id="265f4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="265f4-116">-Force</span></span>
<span data-ttu-id="265f4-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="265f4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="265f4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="265f4-118">-Name</span></span>
<span data-ttu-id="265f4-119">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="265f4-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="265f4-120">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="265f4-120">-PartnerName</span></span>
<span data-ttu-id="265f4-121">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="265f4-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="265f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="265f4-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="265f4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="265f4-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="265f4-124">-Confirm</span></span>
<span data-ttu-id="265f4-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="265f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="265f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="265f4-126">-WhatIf</span></span>
<span data-ttu-id="265f4-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="265f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="265f4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="265f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="265f4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265f4-129">-DefaultProfile</span></span>
<span data-ttu-id="265f4-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="265f4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="265f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265f4-131">CommonParameters</span></span>
<span data-ttu-id="265f4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="265f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265f4-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="265f4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265f4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="265f4-134">INPUTS</span></span>

## <span data-ttu-id="265f4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="265f4-135">OUTPUTS</span></span>

## <span data-ttu-id="265f4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="265f4-136">NOTES</span></span>

## <span data-ttu-id="265f4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="265f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="265f4-138">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="265f4-138">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="265f4-139">Új – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="265f4-139">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="265f4-140">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="265f4-140">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


