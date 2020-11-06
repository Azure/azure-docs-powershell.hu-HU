---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493479"
---
# <span data-ttu-id="c1d13-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1d13-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="c1d13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1d13-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d13-103">Bekerül az integrációs fiókokba.</span><span class="sxs-lookup"><span data-stu-id="c1d13-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1d13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1d13-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1d13-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d13-106">A **Get-AzureRmIntegrationAccount** parancsmag egy erőforráscsoport integrációs fiókjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1d13-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="c1d13-107">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c1d13-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="c1d13-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c1d13-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1d13-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c1d13-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1d13-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c1d13-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1d13-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c1d13-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1d13-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c1d13-112">EXAMPLES</span></span>

### <span data-ttu-id="c1d13-113">Példa 1: integrációs fiók beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="c1d13-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c1d13-114">Ez a parancs a megadott erőforráscsoport IntegrationAccount31 nevű integrációs fiókját kapja.</span><span class="sxs-lookup"><span data-stu-id="c1d13-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="c1d13-115">2. példa: integrációs fiókok beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="c1d13-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c1d13-116">Ez a parancs a ResourceGroup11 nevű erőforráscsoport integrációs fiókjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1d13-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c1d13-117">3. példa: az összes integrációs fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1d13-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c1d13-118">Ez a parancs az Azure-előfizetés összes integrációs fiókját bekapja.</span><span class="sxs-lookup"><span data-stu-id="c1d13-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="c1d13-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1d13-119">PARAMETERS</span></span>

### <span data-ttu-id="c1d13-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1d13-120">-Name</span></span>
<span data-ttu-id="c1d13-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1d13-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c1d13-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d13-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1d13-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1d13-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1d13-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d13-124">-DefaultProfile</span></span>
<span data-ttu-id="c1d13-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1d13-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d13-126">CommonParameters</span></span>
<span data-ttu-id="c1d13-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1d13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d13-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d13-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d13-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d13-129">INPUTS</span></span>

## <span data-ttu-id="c1d13-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d13-130">OUTPUTS</span></span>

### <span data-ttu-id="c1d13-131">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1d13-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c1d13-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1d13-132">NOTES</span></span>

## <span data-ttu-id="c1d13-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1d13-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1d13-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c1d13-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="c1d13-135">Új – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1d13-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="c1d13-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1d13-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="c1d13-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1d13-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


