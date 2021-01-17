---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364208"
---
# <span data-ttu-id="59b2c-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="59b2c-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="59b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="59b2c-103">Integrációs fióktérképet kap.</span><span class="sxs-lookup"><span data-stu-id="59b2c-103">Gets an integration account map.</span></span>

## <span data-ttu-id="59b2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59b2c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b2c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="59b2c-106">A **Get-AzIntegrationAccountMap** parancsmag integrációs fióktérképet kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="59b2c-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="59b2c-107">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét és a leképezés nevét.</span><span class="sxs-lookup"><span data-stu-id="59b2c-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="59b2c-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="59b2c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="59b2c-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="59b2c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="59b2c-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="59b2c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="59b2c-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="59b2c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="59b2c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59b2c-112">EXAMPLES</span></span>

### <span data-ttu-id="59b2c-113">1. példa: Integrációs fiók térképének lekérte</span><span class="sxs-lookup"><span data-stu-id="59b2c-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="59b2c-114">Ez a parancs egy IntegrationAccountMap47 nevű integrációs fióktérképet kap a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="59b2c-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="59b2c-115">2. példa: Integrációs fióktérképek lekérte az integrációs fiók nevét</span><span class="sxs-lookup"><span data-stu-id="59b2c-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="59b2c-116">Ez a parancs az integrációs fiók térképeit az integrációs fiók neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59b2c-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="59b2c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59b2c-117">PARAMETERS</span></span>

### <span data-ttu-id="59b2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b2c-118">-DefaultProfile</span></span>
<span data-ttu-id="59b2c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59b2c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59b2c-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="59b2c-120">-MapName</span></span>
<span data-ttu-id="59b2c-121">Egy integrációs fiók térképének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b2c-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="59b2c-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="59b2c-122">-MapType</span></span>
<span data-ttu-id="59b2c-123">Az integrációs fiók térképtípusa.</span><span class="sxs-lookup"><span data-stu-id="59b2c-123">The integration account map type.</span></span>

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

### <span data-ttu-id="59b2c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="59b2c-124">-Name</span></span>
<span data-ttu-id="59b2c-125">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b2c-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="59b2c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b2c-126">-ResourceGroupName</span></span>
<span data-ttu-id="59b2c-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b2c-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="59b2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b2c-128">CommonParameters</span></span>
<span data-ttu-id="59b2c-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b2c-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b2c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b2c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59b2c-131">INPUTS</span></span>

### <span data-ttu-id="59b2c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="59b2c-132">System.String</span></span>

## <span data-ttu-id="59b2c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b2c-133">OUTPUTS</span></span>

### <span data-ttu-id="59b2c-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="59b2c-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="59b2c-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59b2c-135">NOTES</span></span>

## <span data-ttu-id="59b2c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59b2c-136">RELATED LINKS</span></span>

[<span data-ttu-id="59b2c-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="59b2c-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="59b2c-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="59b2c-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="59b2c-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="59b2c-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


