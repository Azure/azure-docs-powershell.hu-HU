---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469442"
---
# <span data-ttu-id="8620c-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8620c-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="8620c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8620c-102">SYNOPSIS</span></span>
<span data-ttu-id="8620c-103">Módosít egy integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="8620c-103">Modifies an integration account.</span></span>

## <span data-ttu-id="8620c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8620c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8620c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8620c-105">DESCRIPTION</span></span>
<span data-ttu-id="8620c-106">A **Set-AzIntegrationAccount** parancsmag módosítja az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="8620c-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="8620c-107">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiókot képviseli.</span><span class="sxs-lookup"><span data-stu-id="8620c-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="8620c-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="8620c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8620c-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="8620c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8620c-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="8620c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8620c-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="8620c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8620c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8620c-112">EXAMPLES</span></span>

### <span data-ttu-id="8620c-113">1. példa: Integrációs fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="8620c-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="8620c-114">Ez a parancs módosítja az IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8620c-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="8620c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8620c-115">PARAMETERS</span></span>

### <span data-ttu-id="8620c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8620c-116">-DefaultProfile</span></span>
<span data-ttu-id="8620c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8620c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8620c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8620c-118">-Force</span></span>
<span data-ttu-id="8620c-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8620c-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8620c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="8620c-120">-Location</span></span>
<span data-ttu-id="8620c-121">Megadja az integrációs fiók helyét.</span><span class="sxs-lookup"><span data-stu-id="8620c-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="8620c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8620c-122">-Name</span></span>
<span data-ttu-id="8620c-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8620c-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8620c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8620c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8620c-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8620c-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8620c-126">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="8620c-126">-Sku</span></span>
<span data-ttu-id="8620c-127">Megadja az integrációs fiók termékváltozatnevét.</span><span class="sxs-lookup"><span data-stu-id="8620c-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="8620c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8620c-128">-Confirm</span></span>
<span data-ttu-id="8620c-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8620c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8620c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8620c-130">-WhatIf</span></span>
<span data-ttu-id="8620c-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8620c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8620c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8620c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8620c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8620c-133">CommonParameters</span></span>
<span data-ttu-id="8620c-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8620c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8620c-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8620c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8620c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8620c-136">INPUTS</span></span>

### <span data-ttu-id="8620c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8620c-137">System.String</span></span>

## <span data-ttu-id="8620c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8620c-138">OUTPUTS</span></span>

### <span data-ttu-id="8620c-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8620c-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="8620c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8620c-140">NOTES</span></span>

## <span data-ttu-id="8620c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8620c-141">RELATED LINKS</span></span>

[<span data-ttu-id="8620c-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8620c-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="8620c-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8620c-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="8620c-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8620c-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


