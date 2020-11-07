---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: c1f96d462d1556078159d70a47a9869ec21a0e63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666077"
---
# <span data-ttu-id="dbd72-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbd72-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="dbd72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbd72-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd72-103">Bekerül az integrációs fiók partnereibe.</span><span class="sxs-lookup"><span data-stu-id="dbd72-103">Gets integration account partners.</span></span>

## <span data-ttu-id="dbd72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbd72-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbd72-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd72-106">A **Get-AzIntegrationAccountPartner** parancsmag egy erőforráscsoport integrációs partnereivel válik elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="dbd72-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="dbd72-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="dbd72-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="dbd72-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="dbd72-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dbd72-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="dbd72-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dbd72-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="dbd72-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dbd72-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="dbd72-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dbd72-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dbd72-112">EXAMPLES</span></span>

### <span data-ttu-id="dbd72-113">Példa 1: integrációs fiókpartner beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbd72-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="dbd72-114">Ez a parancs beolvassa a IntegrationAccountPartner22 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="dbd72-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="dbd72-115">2. példa: integrációs fiókkal rendelkező partnerek beszerzése az integrációs fiók nevének használatával</span><span class="sxs-lookup"><span data-stu-id="dbd72-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="dbd72-116">Ez a parancs beilleszti a IntegrationAccount31 nevű integrációs fiók integrációs fiókjának partnereit.</span><span class="sxs-lookup"><span data-stu-id="dbd72-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="dbd72-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbd72-117">PARAMETERS</span></span>

### <span data-ttu-id="dbd72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd72-118">-DefaultProfile</span></span>
<span data-ttu-id="dbd72-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dbd72-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbd72-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbd72-120">-Name</span></span>
<span data-ttu-id="dbd72-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbd72-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="dbd72-122">-PartnerName</span></span>
<span data-ttu-id="dbd72-123">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbd72-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd72-124">-ResourceGroupName</span></span>
<span data-ttu-id="dbd72-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbd72-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd72-126">CommonParameters</span></span>
<span data-ttu-id="dbd72-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbd72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd72-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd72-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbd72-129">INPUTS</span></span>

### <span data-ttu-id="dbd72-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd72-130">System.String</span></span>

## <span data-ttu-id="dbd72-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbd72-131">OUTPUTS</span></span>

### <span data-ttu-id="dbd72-132">Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbd72-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="dbd72-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbd72-133">NOTES</span></span>

## <span data-ttu-id="dbd72-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbd72-134">RELATED LINKS</span></span>

[<span data-ttu-id="dbd72-135">Új – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbd72-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="dbd72-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbd72-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="dbd72-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbd72-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


