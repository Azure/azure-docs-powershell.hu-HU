---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4dea211f2a09823161c1c6551b1fa00ab018a855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666011"
---
# <span data-ttu-id="89239-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="89239-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="89239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89239-102">SYNOPSIS</span></span>
<span data-ttu-id="89239-103">Frissíti az Adathozzáférési fiók által generált bankközi vezérlő számot (NVH) az Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="89239-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="89239-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89239-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89239-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89239-105">DESCRIPTION</span></span>
<span data-ttu-id="89239-106">A Set-AzIntegrationAccountGeneratedIcn parancsmag egy meglévő, az integrációt szabályozó számot (NVH) frissít, és egy olyan objektumot ad eredményül, amely a bankközi vezérlő által generált integrációs fiókot képviseli.</span><span class="sxs-lookup"><span data-stu-id="89239-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="89239-107">Ezzel a parancsmaggal frissítheti az adatintegrációs fiókok által generált bankközi vezérlő számát.</span><span class="sxs-lookup"><span data-stu-id="89239-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="89239-108">Az integrációs fiókokat az integrációs fiók nevének, az erőforráscsoport nevének és a szerződés nevének megadásával frissítheti.</span><span class="sxs-lookup"><span data-stu-id="89239-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="89239-109">Ehhez a parancshoz nem hozható létre új integrációs fiók.</span><span class="sxs-lookup"><span data-stu-id="89239-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="89239-110">Ha a dinamikus paramétereket szeretné használni, csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzéséhez, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="89239-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="89239-111">Ha kihagy egy szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="89239-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="89239-112">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="89239-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="89239-113">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="89239-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="89239-114">Példák</span><span class="sxs-lookup"><span data-stu-id="89239-114">EXAMPLES</span></span>

### <span data-ttu-id="89239-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89239-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="89239-116">Ez a parancs beilleszti az integrációs fiókot, amely egy adott integrációs X12 generálta az adatcsere-vezérlési számot egy adott integrációs fiókra vonatkozó szerződéshez, az 100 értékét a módosított értékre</span><span class="sxs-lookup"><span data-stu-id="89239-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="89239-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="89239-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="89239-118">Ez a parancs beilleszti az integrációs fiókot, amely egy adott integrációs EdifactIntegrationAccountAgreement generálta az adatcsere-vezérlési számot egy adott integrációs fiókra vonatkozó szerződéshez, az 100 értékét a módosított értékre</span><span class="sxs-lookup"><span data-stu-id="89239-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="89239-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89239-119">PARAMETERS</span></span>

### <span data-ttu-id="89239-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="89239-120">-AgreementName</span></span>
<span data-ttu-id="89239-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="89239-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="89239-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="89239-122">-AgreementType</span></span>
<span data-ttu-id="89239-123">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="89239-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89239-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="89239-124">-ControlNumber</span></span>
<span data-ttu-id="89239-125">A generált vezérlőelem száma új érték.</span><span class="sxs-lookup"><span data-stu-id="89239-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="89239-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89239-126">-DefaultProfile</span></span>
<span data-ttu-id="89239-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89239-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89239-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89239-128">-Name</span></span>
<span data-ttu-id="89239-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="89239-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89239-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89239-130">-ResourceGroupName</span></span>
<span data-ttu-id="89239-131">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="89239-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="89239-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89239-132">-Confirm</span></span>
<span data-ttu-id="89239-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89239-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89239-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89239-134">-WhatIf</span></span>
<span data-ttu-id="89239-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89239-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89239-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89239-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89239-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89239-137">CommonParameters</span></span>
<span data-ttu-id="89239-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89239-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89239-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89239-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89239-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89239-140">INPUTS</span></span>

### <span data-ttu-id="89239-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89239-141">System.String</span></span>

## <span data-ttu-id="89239-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89239-142">OUTPUTS</span></span>

### <span data-ttu-id="89239-143">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="89239-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="89239-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89239-144">NOTES</span></span>

## <span data-ttu-id="89239-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89239-145">RELATED LINKS</span></span>

[<span data-ttu-id="89239-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="89239-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

