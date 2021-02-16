---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154842"
---
# <span data-ttu-id="51bd0-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="51bd0-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="51bd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="51bd0-103">Eltávolít egy integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="51bd0-103">Removes an integration account.</span></span>

## <span data-ttu-id="51bd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51bd0-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bd0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="51bd0-106">A **Remove-AzIntegrationAccount** parancsmag eltávolít egy integrációs fiókot egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="51bd0-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="51bd0-107">Adja meg az integrációs fiók nevét és az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="51bd0-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="51bd0-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="51bd0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="51bd0-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="51bd0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="51bd0-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="51bd0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="51bd0-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="51bd0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="51bd0-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51bd0-112">EXAMPLES</span></span>

### <span data-ttu-id="51bd0-113">1. példa: Integrációs fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51bd0-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="51bd0-114">Ez a parancs eltávolít egy IntegrationAccount31 nevű integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="51bd0-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="51bd0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51bd0-115">PARAMETERS</span></span>

### <span data-ttu-id="51bd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bd0-116">-DefaultProfile</span></span>
<span data-ttu-id="51bd0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="51bd0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51bd0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="51bd0-118">-Force</span></span>
<span data-ttu-id="51bd0-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="51bd0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51bd0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="51bd0-120">-Name</span></span>
<span data-ttu-id="51bd0-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bd0-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="51bd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51bd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="51bd0-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51bd0-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="51bd0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51bd0-124">-Confirm</span></span>
<span data-ttu-id="51bd0-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="51bd0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51bd0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bd0-126">-WhatIf</span></span>
<span data-ttu-id="51bd0-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="51bd0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51bd0-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51bd0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51bd0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bd0-129">CommonParameters</span></span>
<span data-ttu-id="51bd0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bd0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bd0-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bd0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bd0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51bd0-132">INPUTS</span></span>

### <span data-ttu-id="51bd0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51bd0-133">System.String</span></span>

## <span data-ttu-id="51bd0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51bd0-134">OUTPUTS</span></span>

### <span data-ttu-id="51bd0-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="51bd0-135">System.Void</span></span>

## <span data-ttu-id="51bd0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51bd0-136">NOTES</span></span>

## <span data-ttu-id="51bd0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51bd0-137">RELATED LINKS</span></span>

[<span data-ttu-id="51bd0-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="51bd0-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="51bd0-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="51bd0-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="51bd0-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="51bd0-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


