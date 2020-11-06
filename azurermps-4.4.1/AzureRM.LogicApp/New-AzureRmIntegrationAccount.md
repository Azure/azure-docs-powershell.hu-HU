---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501807"
---
# <span data-ttu-id="462a9-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="462a9-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="462a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="462a9-102">SYNOPSIS</span></span>
<span data-ttu-id="462a9-103">Integrációs fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="462a9-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="462a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="462a9-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="462a9-105">DESCRIPTION</span></span>
<span data-ttu-id="462a9-106">A **New-AzureRmIntegrationAccount** parancsmag egy integrációs fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="462a9-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="462a9-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókot jelképezi. Adjon meg egy nevet, helyet, erőforrás-csoportot és SKU-nevet.</span><span class="sxs-lookup"><span data-stu-id="462a9-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="462a9-108">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="462a9-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="462a9-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="462a9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="462a9-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="462a9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="462a9-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="462a9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="462a9-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="462a9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="462a9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="462a9-113">EXAMPLES</span></span>

### <span data-ttu-id="462a9-114">Példa 1: integrációs fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="462a9-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="462a9-115">Ez a parancs létrehoz egy IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="462a9-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="462a9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="462a9-116">PARAMETERS</span></span>

### <span data-ttu-id="462a9-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="462a9-117">-Location</span></span>
<span data-ttu-id="462a9-118">Az integrációs fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="462a9-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="462a9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="462a9-119">-Name</span></span>
<span data-ttu-id="462a9-120">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="462a9-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="462a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="462a9-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="462a9-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="462a9-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="462a9-123">-Sku</span></span>
<span data-ttu-id="462a9-124">Az integrációs fiók SKU-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="462a9-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="462a9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="462a9-125">-Confirm</span></span>
<span data-ttu-id="462a9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="462a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462a9-127">-WhatIf</span></span>
<span data-ttu-id="462a9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="462a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462a9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="462a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462a9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462a9-130">-DefaultProfile</span></span>
<span data-ttu-id="462a9-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="462a9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="462a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462a9-132">CommonParameters</span></span>
<span data-ttu-id="462a9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="462a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462a9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462a9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="462a9-135">INPUTS</span></span>

## <span data-ttu-id="462a9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="462a9-136">OUTPUTS</span></span>

### <span data-ttu-id="462a9-137">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="462a9-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="462a9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="462a9-138">NOTES</span></span>

## <span data-ttu-id="462a9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="462a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="462a9-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="462a9-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="462a9-141">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="462a9-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="462a9-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="462a9-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


