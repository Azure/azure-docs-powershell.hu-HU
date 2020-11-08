---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184499"
---
# <span data-ttu-id="0159e-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0159e-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="0159e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0159e-102">SYNOPSIS</span></span>
<span data-ttu-id="0159e-103">Bekerül az integrációs fiókokba.</span><span class="sxs-lookup"><span data-stu-id="0159e-103">Gets integration accounts.</span></span>

## <span data-ttu-id="0159e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0159e-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0159e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0159e-105">DESCRIPTION</span></span>
<span data-ttu-id="0159e-106">A **Get-AzIntegrationAccount** parancsmag egy erőforráscsoport integrációs fiókjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0159e-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="0159e-107">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0159e-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="0159e-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0159e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0159e-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0159e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0159e-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="0159e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0159e-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="0159e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0159e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0159e-112">EXAMPLES</span></span>

### <span data-ttu-id="0159e-113">Példa 1: integrációs fiók beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="0159e-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="0159e-114">Ez a parancs a megadott erőforráscsoport IntegrationAccount31 nevű integrációs fiókját kapja.</span><span class="sxs-lookup"><span data-stu-id="0159e-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="0159e-115">2. példa: integrációs fiókok beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="0159e-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="0159e-116">Ez a parancs a ResourceGroup11 nevű erőforráscsoport integrációs fiókjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0159e-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="0159e-117">3. példa: az összes integrációs fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="0159e-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="0159e-118">Ez a parancs az Azure-előfizetés összes integrációs fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="0159e-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="0159e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0159e-119">PARAMETERS</span></span>

### <span data-ttu-id="0159e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0159e-120">-DefaultProfile</span></span>
<span data-ttu-id="0159e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0159e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0159e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0159e-122">-Name</span></span>
<span data-ttu-id="0159e-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0159e-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="0159e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0159e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0159e-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0159e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0159e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0159e-126">CommonParameters</span></span>
<span data-ttu-id="0159e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0159e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0159e-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0159e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0159e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0159e-129">INPUTS</span></span>

### <span data-ttu-id="0159e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0159e-130">System.String</span></span>

## <span data-ttu-id="0159e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0159e-131">OUTPUTS</span></span>

### <span data-ttu-id="0159e-132">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0159e-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="0159e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0159e-133">NOTES</span></span>

## <span data-ttu-id="0159e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0159e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0159e-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0159e-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="0159e-136">Új – AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0159e-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="0159e-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0159e-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="0159e-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0159e-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


