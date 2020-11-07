---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: b1833f2a87f21df7f7826ad395564fd4fe4151be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666037"
---
# <span data-ttu-id="0423e-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0423e-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="0423e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0423e-102">SYNOPSIS</span></span>
<span data-ttu-id="0423e-103">Egy integrációs fiók eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0423e-103">Removes an integration account.</span></span>

## <span data-ttu-id="0423e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0423e-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0423e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0423e-105">DESCRIPTION</span></span>
<span data-ttu-id="0423e-106">A **Remove-AzIntegrationAccount** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="0423e-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="0423e-107">Adja meg az integrációs fiók nevét és az erőforrás csoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0423e-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="0423e-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0423e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0423e-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0423e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0423e-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="0423e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0423e-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="0423e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0423e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0423e-112">EXAMPLES</span></span>

### <span data-ttu-id="0423e-113">1. példa: az integrációs fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0423e-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="0423e-114">Ez a parancs eltávolítja a IntegrationAccount31 nevű integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="0423e-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="0423e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0423e-115">PARAMETERS</span></span>

### <span data-ttu-id="0423e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0423e-116">-DefaultProfile</span></span>
<span data-ttu-id="0423e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0423e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0423e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0423e-118">-Force</span></span>
<span data-ttu-id="0423e-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0423e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0423e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0423e-120">-Name</span></span>
<span data-ttu-id="0423e-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0423e-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0423e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0423e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0423e-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0423e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0423e-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0423e-124">-Confirm</span></span>
<span data-ttu-id="0423e-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0423e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0423e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0423e-126">-WhatIf</span></span>
<span data-ttu-id="0423e-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0423e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0423e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0423e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0423e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0423e-129">CommonParameters</span></span>
<span data-ttu-id="0423e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0423e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0423e-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0423e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0423e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0423e-132">INPUTS</span></span>

### <span data-ttu-id="0423e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0423e-133">System.String</span></span>

## <span data-ttu-id="0423e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0423e-134">OUTPUTS</span></span>

### <span data-ttu-id="0423e-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="0423e-135">System.Void</span></span>

## <span data-ttu-id="0423e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0423e-136">NOTES</span></span>

## <span data-ttu-id="0423e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0423e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0423e-138">Új – AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0423e-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="0423e-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0423e-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="0423e-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0423e-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


