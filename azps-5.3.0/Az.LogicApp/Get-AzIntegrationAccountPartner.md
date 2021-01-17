---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480070"
---
# <span data-ttu-id="a58c2-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a58c2-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="a58c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a58c2-103">Integrációs fiókpartnereket kap.</span><span class="sxs-lookup"><span data-stu-id="a58c2-103">Gets integration account partners.</span></span>

## <span data-ttu-id="a58c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a58c2-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58c2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a58c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a58c2-106">A **Get-AzIntegrationAccountPartner** parancsmag integrációs fiókpartnereket kap egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="a58c2-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="a58c2-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="a58c2-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="a58c2-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a58c2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a58c2-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="a58c2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a58c2-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="a58c2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a58c2-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="a58c2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a58c2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a58c2-112">EXAMPLES</span></span>

### <span data-ttu-id="a58c2-113">1. példa: Integrációs fiók partnerének lekérte</span><span class="sxs-lookup"><span data-stu-id="a58c2-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="a58c2-114">Ez a parancs az IntegrationAccountPartner22 nevű integrációs partnert kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a58c2-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="a58c2-115">2. példa: Integrációs fiók partnerének lekérte egy integrációs fiók nevét használva</span><span class="sxs-lookup"><span data-stu-id="a58c2-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="a58c2-116">Ez a parancs az IntegrationAccount31 nevű integrációs fiók partnerét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a58c2-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="a58c2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a58c2-117">PARAMETERS</span></span>

### <span data-ttu-id="a58c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58c2-118">-DefaultProfile</span></span>
<span data-ttu-id="a58c2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a58c2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a58c2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a58c2-120">-Name</span></span>
<span data-ttu-id="a58c2-121">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a58c2-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="a58c2-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="a58c2-122">-PartnerName</span></span>
<span data-ttu-id="a58c2-123">Az integrációs fiók partnerének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a58c2-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="a58c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a58c2-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a58c2-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a58c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58c2-126">CommonParameters</span></span>
<span data-ttu-id="a58c2-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58c2-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58c2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58c2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a58c2-129">INPUTS</span></span>

### <span data-ttu-id="a58c2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a58c2-130">System.String</span></span>

## <span data-ttu-id="a58c2-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a58c2-131">OUTPUTS</span></span>

### <span data-ttu-id="a58c2-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a58c2-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="a58c2-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a58c2-133">NOTES</span></span>

## <span data-ttu-id="a58c2-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a58c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a58c2-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a58c2-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a58c2-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a58c2-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a58c2-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a58c2-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


