---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: f56878ac2aa2f625b5583805150fd16368d9f718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503624"
---
# <span data-ttu-id="c8fdf-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8fdf-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="c8fdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fdf-103">Megkapja az integrációs fiók térképét.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8fdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8fdf-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8fdf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="c8fdf-106">A **Get-AzureRmIntegrationAccountMap** parancsmag egy erőforráscsoport integrációs fiókjának térképét kapja.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="c8fdf-107">Az integrációs fiók nevének, az erőforrás csoport nevének és a megfeleltetés nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="c8fdf-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c8fdf-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c8fdf-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c8fdf-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c8fdf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c8fdf-112">EXAMPLES</span></span>

### <span data-ttu-id="c8fdf-113">Példa 1: integrációs fiók térképének beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8fdf-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="c8fdf-114">Ez a parancs a megadott erőforráscsoport IntegrationAccountMap47 nevű integrációs fiókját kapja.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="c8fdf-115">2. példa: az integrációs fiók megfeleltetésének beszerzése az integrációs fiók nevével</span><span class="sxs-lookup"><span data-stu-id="c8fdf-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="c8fdf-116">Ez a parancs az integrációs fiók nevével kapja meg az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="c8fdf-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8fdf-117">PARAMETERS</span></span>

### <span data-ttu-id="c8fdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8fdf-118">-DefaultProfile</span></span>
<span data-ttu-id="c8fdf-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8fdf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8fdf-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="c8fdf-120">-MapName</span></span>
<span data-ttu-id="c8fdf-121">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="c8fdf-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8fdf-122">-Name</span></span>
<span data-ttu-id="c8fdf-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="c8fdf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8fdf-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8fdf-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c8fdf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fdf-126">CommonParameters</span></span>
<span data-ttu-id="c8fdf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8fdf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fdf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8fdf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fdf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8fdf-129">INPUTS</span></span>

### <span data-ttu-id="c8fdf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c8fdf-130">System.String</span></span>

## <span data-ttu-id="c8fdf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8fdf-131">OUTPUTS</span></span>

### <span data-ttu-id="c8fdf-132">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8fdf-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="c8fdf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8fdf-133">NOTES</span></span>

## <span data-ttu-id="c8fdf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8fdf-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8fdf-135">Új – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8fdf-135">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="c8fdf-136">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8fdf-136">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="c8fdf-137">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8fdf-137">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)

