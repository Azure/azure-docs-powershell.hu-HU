---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194667"
---
# <span data-ttu-id="32cff-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="32cff-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="32cff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32cff-102">SYNOPSIS</span></span>
<span data-ttu-id="32cff-103">Az integrációs fiók sémájának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="32cff-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="32cff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32cff-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32cff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32cff-105">DESCRIPTION</span></span>
<span data-ttu-id="32cff-106">A **Remove-AzIntegrationAccountSchema** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók sémáját.</span><span class="sxs-lookup"><span data-stu-id="32cff-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="32cff-107">Az integrációs fiók nevének, az erőforrás csoport nevének és a séma nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="32cff-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="32cff-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="32cff-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="32cff-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="32cff-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="32cff-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="32cff-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="32cff-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="32cff-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="32cff-112">Példák</span><span class="sxs-lookup"><span data-stu-id="32cff-112">EXAMPLES</span></span>

### <span data-ttu-id="32cff-113">1. példa: az integrációs fiók sémájának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="32cff-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="32cff-114">Ez a parancs eltávolítja a IntegrationAccountSchema43 nevű integrációs fiók sémát.</span><span class="sxs-lookup"><span data-stu-id="32cff-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="32cff-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32cff-115">PARAMETERS</span></span>

### <span data-ttu-id="32cff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cff-116">-DefaultProfile</span></span>
<span data-ttu-id="32cff-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32cff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32cff-118">-Force</span><span class="sxs-lookup"><span data-stu-id="32cff-118">-Force</span></span>
<span data-ttu-id="32cff-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="32cff-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32cff-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32cff-120">-Name</span></span>
<span data-ttu-id="32cff-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32cff-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="32cff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cff-122">-ResourceGroupName</span></span>
<span data-ttu-id="32cff-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32cff-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="32cff-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="32cff-124">-SchemaName</span></span>
<span data-ttu-id="32cff-125">Az integrációs fiók sémájának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32cff-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="32cff-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32cff-126">-Confirm</span></span>
<span data-ttu-id="32cff-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32cff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32cff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32cff-128">-WhatIf</span></span>
<span data-ttu-id="32cff-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32cff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32cff-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32cff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32cff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cff-131">CommonParameters</span></span>
<span data-ttu-id="32cff-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32cff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cff-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32cff-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cff-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32cff-134">INPUTS</span></span>

### <span data-ttu-id="32cff-135">System. String</span><span class="sxs-lookup"><span data-stu-id="32cff-135">System.String</span></span>

## <span data-ttu-id="32cff-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32cff-136">OUTPUTS</span></span>

### <span data-ttu-id="32cff-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="32cff-137">System.Void</span></span>

## <span data-ttu-id="32cff-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32cff-138">NOTES</span></span>

## <span data-ttu-id="32cff-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32cff-139">RELATED LINKS</span></span>

[<span data-ttu-id="32cff-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="32cff-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="32cff-141">Új – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="32cff-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="32cff-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="32cff-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


