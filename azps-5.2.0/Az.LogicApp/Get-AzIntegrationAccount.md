---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329219"
---
# <span data-ttu-id="d9c4a-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d9c4a-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="d9c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c4a-103">Integrációs fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-103">Gets integration accounts.</span></span>

## <span data-ttu-id="d9c4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9c4a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9c4a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c4a-106">A **Get-AzIntegrationAccount** parancsmag integrációs fiókokat kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="d9c4a-107">Adja meg az integrációs fiók és az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="d9c4a-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d9c4a-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d9c4a-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d9c4a-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d9c4a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9c4a-112">EXAMPLES</span></span>

### <span data-ttu-id="d9c4a-113">1. példa: Integrációs fiók létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="d9c4a-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="d9c4a-114">Ez a parancs egy IntegrationAccount31 nevű integrációs fiókot kap a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="d9c4a-115">2. példa: Integrációs fiókok lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="d9c4a-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="d9c4a-116">Ez a parancs integrációs fiókokat kap egy ResourceGroup11 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d9c4a-117">3. példa: Az összes integrációs fiók lekérte</span><span class="sxs-lookup"><span data-stu-id="d9c4a-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="d9c4a-118">Ez a parancs az Azure-előfizetés összes integrációs fiókot beveszi.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="d9c4a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9c4a-119">PARAMETERS</span></span>

### <span data-ttu-id="d9c4a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c4a-120">-DefaultProfile</span></span>
<span data-ttu-id="d9c4a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9c4a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9c4a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d9c4a-122">-Name</span></span>
<span data-ttu-id="d9c4a-123">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d9c4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9c4a-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9c4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c4a-126">CommonParameters</span></span>
<span data-ttu-id="d9c4a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c4a-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c4a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c4a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9c4a-129">INPUTS</span></span>

### <span data-ttu-id="d9c4a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c4a-130">System.String</span></span>

## <span data-ttu-id="d9c4a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9c4a-131">OUTPUTS</span></span>

### <span data-ttu-id="d9c4a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d9c4a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="d9c4a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9c4a-133">NOTES</span></span>

## <span data-ttu-id="d9c4a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9c4a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9c4a-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d9c4a-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="d9c4a-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d9c4a-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="d9c4a-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d9c4a-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="d9c4a-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d9c4a-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


