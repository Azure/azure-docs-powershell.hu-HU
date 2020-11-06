---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: c74f4f89337d8fee4e6739cb145e9d2da0d4b81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493467"
---
# <span data-ttu-id="08bb6-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08bb6-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="08bb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="08bb6-103">Bekerül az integrációs fiók partnereibe.</span><span class="sxs-lookup"><span data-stu-id="08bb6-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08bb6-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08bb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="08bb6-106">A **Get-AzureRmIntegrationAccountPartner** parancsmag egy erőforráscsoport integrációs partnereivel válik elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="08bb6-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="08bb6-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="08bb6-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="08bb6-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="08bb6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="08bb6-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="08bb6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="08bb6-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="08bb6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="08bb6-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="08bb6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="08bb6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="08bb6-112">EXAMPLES</span></span>

### <span data-ttu-id="08bb6-113">Példa 1: integrációs fiókpartner beszerzése</span><span class="sxs-lookup"><span data-stu-id="08bb6-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="08bb6-114">Ez a parancs beolvassa a IntegrationAccountPartner22 nevű integrációs fiókpartner-partnert.</span><span class="sxs-lookup"><span data-stu-id="08bb6-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="08bb6-115">2. példa: integrációs fiókkal rendelkező partnerek beszerzése az integrációs fiók nevének használatával</span><span class="sxs-lookup"><span data-stu-id="08bb6-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="08bb6-116">Ez a parancs beilleszti a IntegrationAccount31 nevű integrációs fiók integrációs fiókjának partnereit.</span><span class="sxs-lookup"><span data-stu-id="08bb6-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="08bb6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08bb6-117">PARAMETERS</span></span>

### <span data-ttu-id="08bb6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08bb6-118">-Name</span></span>
<span data-ttu-id="08bb6-119">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08bb6-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="08bb6-120">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="08bb6-120">-PartnerName</span></span>
<span data-ttu-id="08bb6-121">Az integrációs fiókpartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08bb6-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="08bb6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08bb6-122">-ResourceGroupName</span></span>
<span data-ttu-id="08bb6-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08bb6-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08bb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bb6-124">-DefaultProfile</span></span>
<span data-ttu-id="08bb6-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08bb6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bb6-126">CommonParameters</span></span>
<span data-ttu-id="08bb6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08bb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bb6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bb6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08bb6-129">INPUTS</span></span>

## <span data-ttu-id="08bb6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08bb6-130">OUTPUTS</span></span>

### <span data-ttu-id="08bb6-131">Microsoft. Azure. Management. Logic. models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08bb6-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="08bb6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08bb6-132">NOTES</span></span>

## <span data-ttu-id="08bb6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08bb6-133">RELATED LINKS</span></span>

[<span data-ttu-id="08bb6-134">Új – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08bb6-134">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="08bb6-135">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08bb6-135">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="08bb6-136">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08bb6-136">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


