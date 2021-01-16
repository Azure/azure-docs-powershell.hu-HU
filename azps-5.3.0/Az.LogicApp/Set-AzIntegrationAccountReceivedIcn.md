---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466334"
---
# <span data-ttu-id="360d7-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="360d7-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="360d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="360d7-102">SYNOPSIS</span></span>
<span data-ttu-id="360d7-103">Frissíti az integrációs fiókhoz kapott adatcsere-vezérlőszámot (ICN) az Azure erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="360d7-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="360d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="360d7-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="360d7-105">DESCRIPTION</span></span>
<span data-ttu-id="360d7-106">A Set-AzIntegrationAccountGeneratedIcn parancsmag frissíti a meglévő integrációs fiók ICN-számát, és visszaad egy objektumot, amely az integrációs fiók kapott csomópontvezérlő számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="360d7-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="360d7-107">Ezzel a parancsmagtal frissítheti egy integrációs fiók üzenetfeldolgozási állapotát egy olyan integrációs fiókban, amely megkapta a vezérlőszám üzenetfeldolgozási állapotát.</span><span class="sxs-lookup"><span data-stu-id="360d7-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="360d7-108">Frissítheti az integrációs fiók kapott csomópont-vezérlőszámát az integrációs fiók nevének, az erőforráscsoport nevének, a szerződés nevének, a számérték és az üzenetfeldolgozás állapotának megadásával.</span><span class="sxs-lookup"><span data-stu-id="360d7-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="360d7-109">Ezzel a paranccsal nem hozhat létre új integrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="360d7-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="360d7-110">A dinamikus paraméterek csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzésére, majd nyomja le többször a TAB billentyűt az elérhető paraméterek között való váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="360d7-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="360d7-111">Ha nem ad meg egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="360d7-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="360d7-112">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="360d7-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="360d7-113">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="360d7-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="360d7-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="360d7-114">EXAMPLES</span></span>

### <span data-ttu-id="360d7-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="360d7-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="360d7-116">Ez a parancs frissíti az integrációs fiókhoz kapott X12-es adatcsere-vezérlőszámot egy adott integrációs fiókszerződéshez és az üzenetfeldolgozási állapottal nem sikerült értékhez.</span><span class="sxs-lookup"><span data-stu-id="360d7-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="360d7-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="360d7-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="360d7-118">Ez a parancs frissíti az integrációs fiókhoz kapott Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span><span class="sxs-lookup"><span data-stu-id="360d7-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="360d7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="360d7-119">PARAMETERS</span></span>

### <span data-ttu-id="360d7-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="360d7-120">-AgreementName</span></span>
<span data-ttu-id="360d7-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="360d7-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="360d7-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="360d7-122">-AgreementType</span></span>
<span data-ttu-id="360d7-123">Az integrációs fiók szerződéstípusa (X12 vagy Edifact).</span><span class="sxs-lookup"><span data-stu-id="360d7-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="360d7-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="360d7-124">-ControlNumberValue</span></span>
<span data-ttu-id="360d7-125">Az integrációs fiók vezérlőszámának értéke.</span><span class="sxs-lookup"><span data-stu-id="360d7-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="360d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360d7-126">-DefaultProfile</span></span>
<span data-ttu-id="360d7-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="360d7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="360d7-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="360d7-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="360d7-129">A kapott üzenet feldolgozási állapota.</span><span class="sxs-lookup"><span data-stu-id="360d7-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360d7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="360d7-130">-Name</span></span>
<span data-ttu-id="360d7-131">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="360d7-131">The integration account name.</span></span>

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

### <span data-ttu-id="360d7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360d7-132">-ResourceGroupName</span></span>
<span data-ttu-id="360d7-133">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="360d7-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="360d7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="360d7-134">-Confirm</span></span>
<span data-ttu-id="360d7-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="360d7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360d7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360d7-136">-WhatIf</span></span>
<span data-ttu-id="360d7-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="360d7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360d7-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="360d7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360d7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360d7-139">CommonParameters</span></span>
<span data-ttu-id="360d7-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360d7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360d7-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360d7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360d7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="360d7-142">INPUTS</span></span>

### <span data-ttu-id="360d7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="360d7-143">System.String</span></span>

## <span data-ttu-id="360d7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="360d7-144">OUTPUTS</span></span>

### <span data-ttu-id="360d7-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="360d7-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="360d7-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="360d7-146">NOTES</span></span>

## <span data-ttu-id="360d7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="360d7-147">RELATED LINKS</span></span>

<span data-ttu-id="360d7-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="360d7-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
