---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195843"
---
# <span data-ttu-id="3326f-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3326f-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="3326f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3326f-102">SYNOPSIS</span></span>
<span data-ttu-id="3326f-103">Az integrációs fiókkal kötött szerződés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3326f-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="3326f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3326f-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3326f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3326f-105">DESCRIPTION</span></span>
<span data-ttu-id="3326f-106">A **Remove-AzIntegrationAccountAgreement** parancsmag egy Azure-erőforráscsoport által eltávolított integrációs fiókról szóló szerződést távolít el.</span><span class="sxs-lookup"><span data-stu-id="3326f-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="3326f-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="3326f-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="3326f-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="3326f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3326f-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="3326f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3326f-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="3326f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3326f-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="3326f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3326f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3326f-112">EXAMPLES</span></span>

### <span data-ttu-id="3326f-113">Példa 1: az integrációs fiókkal kötött szerződés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="3326f-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="3326f-114">Ez a parancs eltávolítja a IntegrationAccountAgreement06 nevű integrációs fiók szerződését.</span><span class="sxs-lookup"><span data-stu-id="3326f-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="3326f-115">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3326f-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3326f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3326f-116">PARAMETERS</span></span>

### <span data-ttu-id="3326f-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="3326f-117">-AgreementName</span></span>
<span data-ttu-id="3326f-118">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3326f-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="3326f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3326f-119">-DefaultProfile</span></span>
<span data-ttu-id="3326f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3326f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3326f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3326f-121">-Force</span></span>
<span data-ttu-id="3326f-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3326f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3326f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3326f-123">-Name</span></span>
<span data-ttu-id="3326f-124">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3326f-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3326f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3326f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3326f-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3326f-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3326f-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3326f-127">-Confirm</span></span>
<span data-ttu-id="3326f-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3326f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3326f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3326f-129">-WhatIf</span></span>
<span data-ttu-id="3326f-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3326f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3326f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3326f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3326f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3326f-132">CommonParameters</span></span>
<span data-ttu-id="3326f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3326f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3326f-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3326f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3326f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3326f-135">INPUTS</span></span>

### <span data-ttu-id="3326f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3326f-136">System.String</span></span>

## <span data-ttu-id="3326f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3326f-137">OUTPUTS</span></span>

### <span data-ttu-id="3326f-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="3326f-138">System.Void</span></span>

## <span data-ttu-id="3326f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3326f-139">NOTES</span></span>

## <span data-ttu-id="3326f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3326f-140">RELATED LINKS</span></span>

[<span data-ttu-id="3326f-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3326f-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3326f-142">Új – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3326f-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3326f-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3326f-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)

