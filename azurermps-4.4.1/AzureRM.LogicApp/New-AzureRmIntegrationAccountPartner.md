---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: da4ea8acd09fadbead53d54618f04597795c45c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680875"
---
# <span data-ttu-id="7372d-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7372d-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="7372d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7372d-102">SYNOPSIS</span></span>
<span data-ttu-id="7372d-103">Integrációs fiókpartner létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7372d-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7372d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7372d-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7372d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7372d-105">DESCRIPTION</span></span>
<span data-ttu-id="7372d-106">A **New-AzureRmIntegrationAccountPartner** parancsmag létrehoz egy integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="7372d-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="7372d-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókpartner.</span><span class="sxs-lookup"><span data-stu-id="7372d-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="7372d-108">Adja meg az integrációs fiók nevét, az erőforrás csoport nevét, a partner nevét és a partnerek identitását.</span><span class="sxs-lookup"><span data-stu-id="7372d-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="7372d-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="7372d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="7372d-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7372d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7372d-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7372d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7372d-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7372d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7372d-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7372d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7372d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="7372d-114">EXAMPLES</span></span>

### <span data-ttu-id="7372d-115">Példa 1: integrációs fiókpartner létrehozása</span><span class="sxs-lookup"><span data-stu-id="7372d-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="7372d-116">Ezzel a paranccsal létrejön a IntegrationAccountPartner22 nevű integrációs fiókpartner a megadott erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="7372d-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="7372d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7372d-117">PARAMETERS</span></span>

### <span data-ttu-id="7372d-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="7372d-118">-BusinessIdentities</span></span>
<span data-ttu-id="7372d-119">Az integrációs fiókpartner üzleti identitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="7372d-120">Adjon meg egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7372d-120">Specify a hash table.</span></span>

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

### <span data-ttu-id="7372d-121">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7372d-121">-Metadata</span></span>
<span data-ttu-id="7372d-122">A partner metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-122">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="7372d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7372d-123">-Name</span></span>
<span data-ttu-id="7372d-124">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7372d-125">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="7372d-125">-PartnerName</span></span>
<span data-ttu-id="7372d-126">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-126">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="7372d-127">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="7372d-127">-PartnerType</span></span>
<span data-ttu-id="7372d-128">Az integrációs fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-128">Specifies the type of the integration account.</span></span>
<span data-ttu-id="7372d-129">Ez a paraméter a VÁLLALATKÖZI típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="7372d-129">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="7372d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7372d-130">-ResourceGroupName</span></span>
<span data-ttu-id="7372d-131">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7372d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7372d-132">-Confirm</span></span>
<span data-ttu-id="7372d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7372d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7372d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7372d-134">-WhatIf</span></span>
<span data-ttu-id="7372d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7372d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7372d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7372d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7372d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7372d-137">-DefaultProfile</span></span>
<span data-ttu-id="7372d-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7372d-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7372d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7372d-139">CommonParameters</span></span>
<span data-ttu-id="7372d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7372d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7372d-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7372d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7372d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7372d-142">INPUTS</span></span>

## <span data-ttu-id="7372d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7372d-143">OUTPUTS</span></span>

### <span data-ttu-id="7372d-144">Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7372d-144">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="7372d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7372d-145">NOTES</span></span>

## <span data-ttu-id="7372d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7372d-146">RELATED LINKS</span></span>

[<span data-ttu-id="7372d-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7372d-147">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7372d-148">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7372d-148">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7372d-149">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7372d-149">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


