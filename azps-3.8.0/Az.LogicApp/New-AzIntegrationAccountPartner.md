---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: bbd64f1e6df016efe0bdd22bb0ae848c79566edf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845253"
---
# <span data-ttu-id="15623-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="15623-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="15623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15623-102">SYNOPSIS</span></span>
<span data-ttu-id="15623-103">Integrációs fiókpartner létrehozása.</span><span class="sxs-lookup"><span data-stu-id="15623-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="15623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15623-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15623-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15623-105">DESCRIPTION</span></span>
<span data-ttu-id="15623-106">A **New-AzIntegrationAccountPartner** parancsmag létrehoz egy integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="15623-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="15623-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókpartner.</span><span class="sxs-lookup"><span data-stu-id="15623-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="15623-108">Adja meg az integrációs fiók nevét, az erőforrás csoport nevét, a partner nevét és a partnerek identitását.</span><span class="sxs-lookup"><span data-stu-id="15623-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="15623-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="15623-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="15623-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="15623-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="15623-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="15623-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="15623-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="15623-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15623-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="15623-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15623-114">Példák</span><span class="sxs-lookup"><span data-stu-id="15623-114">EXAMPLES</span></span>

### <span data-ttu-id="15623-115">Példa 1: integrációs fiókpartner létrehozása</span><span class="sxs-lookup"><span data-stu-id="15623-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="15623-116">Ezzel a paranccsal létrejön a IntegrationAccountPartner22 nevű integrációs fiókpartner a megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="15623-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="15623-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15623-117">PARAMETERS</span></span>

### <span data-ttu-id="15623-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="15623-118">-BusinessIdentities</span></span>
<span data-ttu-id="15623-119">Az integrációs fiókpartner üzleti identitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="15623-120">Adjon meg egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="15623-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15623-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15623-121">-DefaultProfile</span></span>
<span data-ttu-id="15623-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15623-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15623-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="15623-123">-Metadata</span></span>
<span data-ttu-id="15623-124">A partner metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15623-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15623-125">-Name</span></span>
<span data-ttu-id="15623-126">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15623-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="15623-127">-PartnerName</span></span>
<span data-ttu-id="15623-128">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="15623-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="15623-129">-PartnerType</span></span>
<span data-ttu-id="15623-130">Az integrációs fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="15623-131">Ez a paraméter a VÁLLALATKÖZI típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="15623-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15623-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15623-132">-ResourceGroupName</span></span>
<span data-ttu-id="15623-133">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15623-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15623-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15623-134">-Confirm</span></span>
<span data-ttu-id="15623-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15623-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15623-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15623-136">-WhatIf</span></span>
<span data-ttu-id="15623-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15623-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15623-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15623-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15623-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15623-139">CommonParameters</span></span>
<span data-ttu-id="15623-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15623-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15623-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15623-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15623-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15623-142">INPUTS</span></span>

### <span data-ttu-id="15623-143">System. String</span><span class="sxs-lookup"><span data-stu-id="15623-143">System.String</span></span>

## <span data-ttu-id="15623-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15623-144">OUTPUTS</span></span>

### <span data-ttu-id="15623-145">Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="15623-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="15623-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15623-146">NOTES</span></span>

## <span data-ttu-id="15623-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15623-147">RELATED LINKS</span></span>

[<span data-ttu-id="15623-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="15623-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="15623-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="15623-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="15623-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="15623-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


