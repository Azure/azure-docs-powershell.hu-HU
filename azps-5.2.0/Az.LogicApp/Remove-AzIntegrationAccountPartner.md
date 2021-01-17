---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345966"
---
# <span data-ttu-id="61329-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="61329-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="61329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61329-102">SYNOPSIS</span></span>
<span data-ttu-id="61329-103">Eltávolít egy integrációs partnert.</span><span class="sxs-lookup"><span data-stu-id="61329-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="61329-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61329-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61329-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61329-105">DESCRIPTION</span></span>
<span data-ttu-id="61329-106">A **Remove-AzIntegrationAccountPartner** parancsmag eltávolít egy integrációs partnert egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="61329-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="61329-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="61329-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="61329-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="61329-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61329-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="61329-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61329-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="61329-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61329-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="61329-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61329-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61329-112">EXAMPLES</span></span>

### <span data-ttu-id="61329-113">1. példa: Integrációs fiók partnerének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61329-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="61329-114">Ez a parancs eltávolítja az IntegrationAccountPartner1 nevű integrációs partnert.</span><span class="sxs-lookup"><span data-stu-id="61329-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="61329-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61329-115">PARAMETERS</span></span>

### <span data-ttu-id="61329-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61329-116">-DefaultProfile</span></span>
<span data-ttu-id="61329-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61329-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61329-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61329-118">-Force</span></span>
<span data-ttu-id="61329-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="61329-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61329-120">-Name</span><span class="sxs-lookup"><span data-stu-id="61329-120">-Name</span></span>
<span data-ttu-id="61329-121">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61329-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61329-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="61329-122">-PartnerName</span></span>
<span data-ttu-id="61329-123">Az integrációs fiók partnerének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61329-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61329-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61329-124">-ResourceGroupName</span></span>
<span data-ttu-id="61329-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61329-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61329-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61329-126">-Confirm</span></span>
<span data-ttu-id="61329-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="61329-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61329-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61329-128">-WhatIf</span></span>
<span data-ttu-id="61329-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="61329-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61329-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61329-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61329-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61329-131">CommonParameters</span></span>
<span data-ttu-id="61329-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61329-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61329-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61329-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61329-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61329-134">INPUTS</span></span>

### <span data-ttu-id="61329-135">System.String</span><span class="sxs-lookup"><span data-stu-id="61329-135">System.String</span></span>

## <span data-ttu-id="61329-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61329-136">OUTPUTS</span></span>

### <span data-ttu-id="61329-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="61329-137">System.Void</span></span>

## <span data-ttu-id="61329-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61329-138">NOTES</span></span>

## <span data-ttu-id="61329-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61329-139">RELATED LINKS</span></span>

[<span data-ttu-id="61329-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="61329-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="61329-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="61329-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="61329-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="61329-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


