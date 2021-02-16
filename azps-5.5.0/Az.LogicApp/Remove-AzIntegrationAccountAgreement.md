---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161443"
---
# <span data-ttu-id="4fb47-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4fb47-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="4fb47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb47-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb47-103">Eltávolít egy integrációs fiókszerződést.</span><span class="sxs-lookup"><span data-stu-id="4fb47-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="4fb47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fb47-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb47-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fb47-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb47-106">A **Remove-AzIntegrationAccountAgreement** parancsmag eltávolít egy integrációs fiókszerződést egy Azure-erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="4fb47-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="4fb47-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="4fb47-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="4fb47-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="4fb47-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4fb47-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="4fb47-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4fb47-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="4fb47-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4fb47-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="4fb47-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4fb47-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fb47-112">EXAMPLES</span></span>

### <span data-ttu-id="4fb47-113">1. példa: Integrációs fiókszerződés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="4fb47-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="4fb47-114">Ez a parancs eltávolítja az IntegrationAccountAgreement06 nevű integrációs fiókszerződést.</span><span class="sxs-lookup"><span data-stu-id="4fb47-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="4fb47-115">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fb47-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4fb47-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fb47-116">PARAMETERS</span></span>

### <span data-ttu-id="4fb47-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="4fb47-117">-AgreementName</span></span>
<span data-ttu-id="4fb47-118">Az integrációs fiókszerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb47-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="4fb47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb47-119">-DefaultProfile</span></span>
<span data-ttu-id="4fb47-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4fb47-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fb47-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4fb47-121">-Force</span></span>
<span data-ttu-id="4fb47-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4fb47-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fb47-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4fb47-123">-Name</span></span>
<span data-ttu-id="4fb47-124">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb47-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="4fb47-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb47-125">-ResourceGroupName</span></span>
<span data-ttu-id="4fb47-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb47-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4fb47-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fb47-127">-Confirm</span></span>
<span data-ttu-id="4fb47-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4fb47-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb47-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb47-129">-WhatIf</span></span>
<span data-ttu-id="4fb47-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4fb47-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb47-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fb47-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb47-132">CommonParameters</span></span>
<span data-ttu-id="4fb47-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb47-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb47-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb47-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fb47-135">INPUTS</span></span>

### <span data-ttu-id="4fb47-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4fb47-136">System.String</span></span>

## <span data-ttu-id="4fb47-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb47-137">OUTPUTS</span></span>

### <span data-ttu-id="4fb47-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="4fb47-138">System.Void</span></span>

## <span data-ttu-id="4fb47-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fb47-139">NOTES</span></span>

## <span data-ttu-id="4fb47-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fb47-140">RELATED LINKS</span></span>

[<span data-ttu-id="4fb47-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4fb47-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="4fb47-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4fb47-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="4fb47-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="4fb47-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


