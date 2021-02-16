---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161459"
---
# <span data-ttu-id="c0caf-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c0caf-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="c0caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0caf-102">SYNOPSIS</span></span>
<span data-ttu-id="c0caf-103">Létrehoz egy integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="c0caf-103">Creates an integration account.</span></span>

## <span data-ttu-id="c0caf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0caf-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0caf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0caf-105">DESCRIPTION</span></span>
<span data-ttu-id="c0caf-106">A **New-AzIntegrationAccount** parancsmag létrehoz egy integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="c0caf-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="c0caf-107">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiókot képviseli. Adja meg a nevet, a helyet, az erőforráscsoport nevét és az termékváltozat nevét.</span><span class="sxs-lookup"><span data-stu-id="c0caf-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="c0caf-108">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterobjektumában megadott paraméterértékekkel.</span><span class="sxs-lookup"><span data-stu-id="c0caf-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c0caf-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c0caf-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c0caf-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c0caf-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c0caf-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="c0caf-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c0caf-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="c0caf-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c0caf-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0caf-113">EXAMPLES</span></span>

### <span data-ttu-id="c0caf-114">1. példa: Integrációs fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0caf-114">Example 1: Create an integration account</span></span>
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

<span data-ttu-id="c0caf-115">Ez a parancs létrehoz egy IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c0caf-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="c0caf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0caf-116">PARAMETERS</span></span>

### <span data-ttu-id="c0caf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0caf-117">-DefaultProfile</span></span>
<span data-ttu-id="c0caf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0caf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0caf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c0caf-119">-Location</span></span>
<span data-ttu-id="c0caf-120">Megadja az integrációs fiók helyét.</span><span class="sxs-lookup"><span data-stu-id="c0caf-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="c0caf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0caf-121">-Name</span></span>
<span data-ttu-id="c0caf-122">Megadja az integrációs fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="c0caf-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="c0caf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0caf-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0caf-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0caf-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c0caf-125">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="c0caf-125">-Sku</span></span>
<span data-ttu-id="c0caf-126">Megadja az integrációs fiók termékváltozatnevét.</span><span class="sxs-lookup"><span data-stu-id="c0caf-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="c0caf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0caf-127">-Confirm</span></span>
<span data-ttu-id="c0caf-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0caf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0caf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0caf-129">-WhatIf</span></span>
<span data-ttu-id="c0caf-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0caf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0caf-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0caf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0caf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0caf-132">CommonParameters</span></span>
<span data-ttu-id="c0caf-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0caf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0caf-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0caf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0caf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0caf-135">INPUTS</span></span>

### <span data-ttu-id="c0caf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c0caf-136">System.String</span></span>

## <span data-ttu-id="c0caf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0caf-137">OUTPUTS</span></span>

### <span data-ttu-id="c0caf-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c0caf-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c0caf-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0caf-139">NOTES</span></span>

## <span data-ttu-id="c0caf-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0caf-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0caf-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c0caf-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="c0caf-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c0caf-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="c0caf-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c0caf-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


