---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195861"
---
# <span data-ttu-id="61840-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61840-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="61840-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61840-102">SYNOPSIS</span></span>
<span data-ttu-id="61840-103">Integrációs fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61840-103">Creates an integration account.</span></span>

## <span data-ttu-id="61840-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61840-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61840-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61840-105">DESCRIPTION</span></span>
<span data-ttu-id="61840-106">A **New-AzIntegrationAccount** parancsmag egy integrációs fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61840-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="61840-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókot jelképezi. Adjon meg egy nevet, helyet, erőforrás-csoportot és SKU-nevet.</span><span class="sxs-lookup"><span data-stu-id="61840-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="61840-108">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="61840-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="61840-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="61840-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61840-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="61840-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61840-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="61840-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61840-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="61840-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61840-113">Példák</span><span class="sxs-lookup"><span data-stu-id="61840-113">EXAMPLES</span></span>

### <span data-ttu-id="61840-114">Példa 1: integrációs fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="61840-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="61840-115">Ez a parancs létrehoz egy IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="61840-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="61840-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61840-116">PARAMETERS</span></span>

### <span data-ttu-id="61840-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61840-117">-DefaultProfile</span></span>
<span data-ttu-id="61840-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61840-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61840-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="61840-119">-Location</span></span>
<span data-ttu-id="61840-120">Az integrációs fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61840-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="61840-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61840-121">-Name</span></span>
<span data-ttu-id="61840-122">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61840-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="61840-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61840-123">-ResourceGroupName</span></span>
<span data-ttu-id="61840-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61840-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61840-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="61840-125">-Sku</span></span>
<span data-ttu-id="61840-126">Az integrációs fiók SKU-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61840-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61840-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61840-127">-Confirm</span></span>
<span data-ttu-id="61840-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61840-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61840-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61840-129">-WhatIf</span></span>
<span data-ttu-id="61840-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61840-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61840-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61840-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61840-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61840-132">CommonParameters</span></span>
<span data-ttu-id="61840-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61840-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61840-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61840-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61840-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61840-135">INPUTS</span></span>

### <span data-ttu-id="61840-136">System. String</span><span class="sxs-lookup"><span data-stu-id="61840-136">System.String</span></span>

## <span data-ttu-id="61840-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61840-137">OUTPUTS</span></span>

### <span data-ttu-id="61840-138">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61840-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="61840-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61840-139">NOTES</span></span>

## <span data-ttu-id="61840-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61840-140">RELATED LINKS</span></span>

[<span data-ttu-id="61840-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61840-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="61840-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61840-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="61840-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61840-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


