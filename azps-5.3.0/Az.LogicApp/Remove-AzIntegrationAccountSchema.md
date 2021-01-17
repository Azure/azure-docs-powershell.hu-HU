---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469462"
---
# <span data-ttu-id="f6732-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f6732-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="f6732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6732-102">SYNOPSIS</span></span>
<span data-ttu-id="f6732-103">Eltávolít egy integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="f6732-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="f6732-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6732-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6732-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6732-105">DESCRIPTION</span></span>
<span data-ttu-id="f6732-106">A **Remove-AzIntegrationAccountSchema** parancsmag eltávolítja az integrációs fióksémát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="f6732-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="f6732-107">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét és a séma nevét.</span><span class="sxs-lookup"><span data-stu-id="f6732-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="f6732-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="f6732-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f6732-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="f6732-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f6732-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="f6732-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f6732-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="f6732-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f6732-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6732-112">EXAMPLES</span></span>

### <span data-ttu-id="f6732-113">1. példa: Integrációs fióksémának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6732-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="f6732-114">Ez a parancs eltávolítja az IntegrationAccountSchema43 nevű integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="f6732-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="f6732-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6732-115">PARAMETERS</span></span>

### <span data-ttu-id="f6732-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6732-116">-DefaultProfile</span></span>
<span data-ttu-id="f6732-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f6732-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6732-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f6732-118">-Force</span></span>
<span data-ttu-id="f6732-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f6732-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6732-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f6732-120">-Name</span></span>
<span data-ttu-id="f6732-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6732-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="f6732-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6732-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6732-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6732-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f6732-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f6732-124">-SchemaName</span></span>
<span data-ttu-id="f6732-125">Egy integrációs fiókséma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6732-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="f6732-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6732-126">-Confirm</span></span>
<span data-ttu-id="f6732-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f6732-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6732-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6732-128">-WhatIf</span></span>
<span data-ttu-id="f6732-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f6732-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6732-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6732-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6732-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6732-131">CommonParameters</span></span>
<span data-ttu-id="f6732-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6732-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6732-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6732-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6732-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6732-134">INPUTS</span></span>

### <span data-ttu-id="f6732-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f6732-135">System.String</span></span>

## <span data-ttu-id="f6732-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6732-136">OUTPUTS</span></span>

### <span data-ttu-id="f6732-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="f6732-137">System.Void</span></span>

## <span data-ttu-id="f6732-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6732-138">NOTES</span></span>

## <span data-ttu-id="f6732-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6732-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6732-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f6732-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="f6732-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f6732-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="f6732-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f6732-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


