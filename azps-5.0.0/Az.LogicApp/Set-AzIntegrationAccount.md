---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194664"
---
# <span data-ttu-id="c19b0-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c19b0-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="c19b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c19b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c19b0-103">Módosítja az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="c19b0-103">Modifies an integration account.</span></span>

## <span data-ttu-id="c19b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c19b0-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19b0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c19b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c19b0-106">A **set-AzIntegrationAccount** parancsmag módosította az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="c19b0-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="c19b0-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiókot jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c19b0-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="c19b0-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c19b0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c19b0-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c19b0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c19b0-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c19b0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c19b0-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c19b0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c19b0-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c19b0-112">EXAMPLES</span></span>

### <span data-ttu-id="c19b0-113">Példa 1: az integrációs fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="c19b0-113">Example 1: Modify an integration account</span></span>
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

<span data-ttu-id="c19b0-114">Ez a parancs módosítja egy IntegrationAccount31 nevű integrációs fiókot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="c19b0-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="c19b0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c19b0-115">PARAMETERS</span></span>

### <span data-ttu-id="c19b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19b0-116">-DefaultProfile</span></span>
<span data-ttu-id="c19b0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c19b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c19b0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c19b0-118">-Force</span></span>
<span data-ttu-id="c19b0-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c19b0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c19b0-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="c19b0-120">-Location</span></span>
<span data-ttu-id="c19b0-121">Az integrációs fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c19b0-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="c19b0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c19b0-122">-Name</span></span>
<span data-ttu-id="c19b0-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c19b0-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="c19b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="c19b0-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c19b0-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c19b0-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c19b0-126">-Sku</span></span>
<span data-ttu-id="c19b0-127">Az integrációs fiók SKU-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c19b0-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="c19b0-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c19b0-128">-Confirm</span></span>
<span data-ttu-id="c19b0-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c19b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19b0-130">-WhatIf</span></span>
<span data-ttu-id="c19b0-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c19b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19b0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c19b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19b0-133">CommonParameters</span></span>
<span data-ttu-id="c19b0-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c19b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19b0-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19b0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19b0-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c19b0-136">INPUTS</span></span>

### <span data-ttu-id="c19b0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c19b0-137">System.String</span></span>

## <span data-ttu-id="c19b0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c19b0-138">OUTPUTS</span></span>

### <span data-ttu-id="c19b0-139">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c19b0-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c19b0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c19b0-140">NOTES</span></span>

## <span data-ttu-id="c19b0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c19b0-141">RELATED LINKS</span></span>

[<span data-ttu-id="c19b0-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c19b0-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="c19b0-143">Új – AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c19b0-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="c19b0-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c19b0-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

