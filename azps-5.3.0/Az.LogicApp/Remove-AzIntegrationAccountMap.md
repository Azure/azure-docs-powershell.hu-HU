---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467666"
---
# <span data-ttu-id="0e18b-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0e18b-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="0e18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e18b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e18b-103">Eltávolít egy integrációs fióktérképet.</span><span class="sxs-lookup"><span data-stu-id="0e18b-103">Removes an integration account map.</span></span>

## <span data-ttu-id="0e18b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e18b-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e18b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e18b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e18b-106">A **Remove-AzIntegrationAccountMap** parancsmag eltávolítja az integrációs fiók leképezését egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="0e18b-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="0e18b-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a leképezés nevét.</span><span class="sxs-lookup"><span data-stu-id="0e18b-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="0e18b-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0e18b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0e18b-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0e18b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0e18b-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="0e18b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0e18b-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="0e18b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0e18b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e18b-112">EXAMPLES</span></span>

### <span data-ttu-id="0e18b-113">1. példa: Integrációs fiók térképének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0e18b-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="0e18b-114">Ez a parancs eltávolítja az IntegrationAccountMap47 nevű integrációs fióktérképet.</span><span class="sxs-lookup"><span data-stu-id="0e18b-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="0e18b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e18b-115">PARAMETERS</span></span>

### <span data-ttu-id="0e18b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e18b-116">-DefaultProfile</span></span>
<span data-ttu-id="0e18b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e18b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e18b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0e18b-118">-Force</span></span>
<span data-ttu-id="0e18b-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0e18b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e18b-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="0e18b-120">-MapName</span></span>
<span data-ttu-id="0e18b-121">Az integrációs fiók térképének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e18b-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="0e18b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0e18b-122">-Name</span></span>
<span data-ttu-id="0e18b-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e18b-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0e18b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e18b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e18b-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e18b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0e18b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e18b-126">-Confirm</span></span>
<span data-ttu-id="0e18b-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e18b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e18b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e18b-128">-WhatIf</span></span>
<span data-ttu-id="0e18b-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e18b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e18b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e18b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e18b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e18b-131">CommonParameters</span></span>
<span data-ttu-id="0e18b-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e18b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e18b-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e18b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e18b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e18b-134">INPUTS</span></span>

### <span data-ttu-id="0e18b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0e18b-135">System.String</span></span>

## <span data-ttu-id="0e18b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e18b-136">OUTPUTS</span></span>

### <span data-ttu-id="0e18b-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="0e18b-137">System.Void</span></span>

## <span data-ttu-id="0e18b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e18b-138">NOTES</span></span>

## <span data-ttu-id="0e18b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e18b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e18b-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0e18b-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="0e18b-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0e18b-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="0e18b-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0e18b-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


