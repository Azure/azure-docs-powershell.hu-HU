---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368435"
---
# <span data-ttu-id="168bd-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="168bd-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="168bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="168bd-102">SYNOPSIS</span></span>
<span data-ttu-id="168bd-103">Frissíti az integrációs fiók által létrehozott adatcsere-vezérlő számát (ICN) az Azure erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="168bd-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="168bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="168bd-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="168bd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="168bd-105">DESCRIPTION</span></span>
<span data-ttu-id="168bd-106">A Set-AzIntegrationAccountGeneratedIcn parancsmag frissíti a meglévő integrációs fiók által létrehozott adatcsere-vezérlőszámot (ICN), és visszaad egy objektumot, amely az integrációs fiók által létrehozott adatcsere-vezérlő számát képviseli.</span><span class="sxs-lookup"><span data-stu-id="168bd-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="168bd-107">Ezzel a parancsmagmal frissítheti az integrációs fiók által létrehozott adatcsere-vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="168bd-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="168bd-108">Frissítheti az integrációs fiók által létrehozott adatcsere-vezérlő számát az integrációs fiók nevének, az erőforráscsoport nevének és a szerződés nevének megadásával.</span><span class="sxs-lookup"><span data-stu-id="168bd-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="168bd-109">Ezzel a paranccsal nem hozhat létre új integrációs fiók által létrehozott adatcsere-vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="168bd-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="168bd-110">A dinamikus paraméterek csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzésére, majd nyomja le többször a TAB billentyűt az elérhető paraméterek között való váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="168bd-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="168bd-111">Ha nem ad meg egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="168bd-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="168bd-112">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="168bd-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="168bd-113">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="168bd-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="168bd-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="168bd-114">EXAMPLES</span></span>

### <span data-ttu-id="168bd-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="168bd-115">Example 1</span></span>
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

<span data-ttu-id="168bd-116">Ez a parancs egy adott integrációs fiók szerződésében létrehozott X12-es integrációs fiók vezérlőszámát kapja meg, 100-sal megnöveli az értékét, majd visszaírja a frissített értéket.</span><span class="sxs-lookup"><span data-stu-id="168bd-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="168bd-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="168bd-117">Example 2</span></span>
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

<span data-ttu-id="168bd-118">Ez a parancs beszerzi egy adott integrációs fiók szerződésének EdifactIntegrationAccountAgreement interchange control numberje által létrehozott EdifactIntegrationAccountAgreement vezérlőelem számát, 100-sal növeli az értékét, majd visszaírja a frissített értéket.</span><span class="sxs-lookup"><span data-stu-id="168bd-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="168bd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="168bd-119">PARAMETERS</span></span>

### <span data-ttu-id="168bd-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="168bd-120">-AgreementName</span></span>
<span data-ttu-id="168bd-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="168bd-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="168bd-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="168bd-122">-AgreementType</span></span>
<span data-ttu-id="168bd-123">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="168bd-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="168bd-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="168bd-124">-ControlNumber</span></span>
<span data-ttu-id="168bd-125">A létrehozott vezérlőszám új értéke.</span><span class="sxs-lookup"><span data-stu-id="168bd-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="168bd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168bd-126">-DefaultProfile</span></span>
<span data-ttu-id="168bd-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="168bd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="168bd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="168bd-128">-Name</span></span>
<span data-ttu-id="168bd-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="168bd-129">The integration account name.</span></span>

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

### <span data-ttu-id="168bd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168bd-130">-ResourceGroupName</span></span>
<span data-ttu-id="168bd-131">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="168bd-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="168bd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="168bd-132">-Confirm</span></span>
<span data-ttu-id="168bd-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="168bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="168bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168bd-134">-WhatIf</span></span>
<span data-ttu-id="168bd-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="168bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168bd-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="168bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="168bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168bd-137">CommonParameters</span></span>
<span data-ttu-id="168bd-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168bd-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168bd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168bd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="168bd-140">INPUTS</span></span>

### <span data-ttu-id="168bd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="168bd-141">System.String</span></span>

## <span data-ttu-id="168bd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="168bd-142">OUTPUTS</span></span>

### <span data-ttu-id="168bd-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="168bd-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="168bd-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="168bd-144">NOTES</span></span>

## <span data-ttu-id="168bd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="168bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="168bd-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="168bd-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

