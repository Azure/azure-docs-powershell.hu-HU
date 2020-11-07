---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845981"
---
# <span data-ttu-id="d660a-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d660a-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="d660a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d660a-102">SYNOPSIS</span></span>
<span data-ttu-id="d660a-103">Megkapja az integrációs fiók térképét.</span><span class="sxs-lookup"><span data-stu-id="d660a-103">Gets an integration account map.</span></span>

## <span data-ttu-id="d660a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d660a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d660a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d660a-105">DESCRIPTION</span></span>
<span data-ttu-id="d660a-106">A **Get-AzIntegrationAccountMap** parancsmag egy erőforráscsoport integrációs fiókjának térképét kapja.</span><span class="sxs-lookup"><span data-stu-id="d660a-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="d660a-107">Az integrációs fiók nevének, az erőforrás csoport nevének és a megfeleltetés nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="d660a-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="d660a-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d660a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d660a-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d660a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d660a-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="d660a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d660a-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="d660a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d660a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d660a-112">EXAMPLES</span></span>

### <span data-ttu-id="d660a-113">Példa 1: integrációs fiók térképének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d660a-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="d660a-114">Ez a parancs a megadott erőforráscsoport IntegrationAccountMap47 nevű integrációs fiókját kapja.</span><span class="sxs-lookup"><span data-stu-id="d660a-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="d660a-115">2. példa: az integrációs fiók megfeleltetésének beszerzése az integrációs fiók nevével</span><span class="sxs-lookup"><span data-stu-id="d660a-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="d660a-116">Ez a parancs az integrációs fiók nevével kapja meg az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="d660a-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="d660a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d660a-117">PARAMETERS</span></span>

### <span data-ttu-id="d660a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d660a-118">-DefaultProfile</span></span>
<span data-ttu-id="d660a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d660a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d660a-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="d660a-120">-MapName</span></span>
<span data-ttu-id="d660a-121">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d660a-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="d660a-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="d660a-122">-MapType</span></span>
<span data-ttu-id="d660a-123">Az integrációs fiók megfeleltetési típusa.</span><span class="sxs-lookup"><span data-stu-id="d660a-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d660a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d660a-124">-Name</span></span>
<span data-ttu-id="d660a-125">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d660a-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="d660a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d660a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d660a-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d660a-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d660a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d660a-128">CommonParameters</span></span>
<span data-ttu-id="d660a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d660a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d660a-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d660a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d660a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d660a-131">INPUTS</span></span>

### <span data-ttu-id="d660a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d660a-132">System.String</span></span>

## <span data-ttu-id="d660a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d660a-133">OUTPUTS</span></span>

### <span data-ttu-id="d660a-134">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d660a-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="d660a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d660a-135">NOTES</span></span>

## <span data-ttu-id="d660a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d660a-136">RELATED LINKS</span></span>

[<span data-ttu-id="d660a-137">Új – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d660a-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="d660a-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d660a-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="d660a-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d660a-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


