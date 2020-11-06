---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 5f25ec9f3b180f6bb0379b399cdbf1a96f9d1f30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503608"
---
# <span data-ttu-id="003a7-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="003a7-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="003a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="003a7-102">SYNOPSIS</span></span>
<span data-ttu-id="003a7-103">Frissíti az integrációs fiókot az Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="003a7-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="003a7-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="003a7-105">DESCRIPTION</span></span>
<span data-ttu-id="003a7-106">A Set-AzureRmIntegrationAccountGeneratedIcn parancsmag egy meglévő, az integrációt szabályozó számot (NVH) tartalmazó meglévő integrációs fiókot frissít, és egy olyan objektumot ad eredményül, amely az integrációs fiókhoz kapott bankközi vezérlő számot jelképezi.</span><span class="sxs-lookup"><span data-stu-id="003a7-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="003a7-107">Ezzel a parancsmaggal frissítheti az integrációs fiókot az adatcsere-vezérlési szám feldolgozási állapotával.</span><span class="sxs-lookup"><span data-stu-id="003a7-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="003a7-108">Az integrációs fiókokat az integrációs fiók nevének, az erőforrás csoport nevének, a szerződés nevének, a vezérlő szám értékének és az üzenet feldolgozási állapotának megadásával frissítheti.</span><span class="sxs-lookup"><span data-stu-id="003a7-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="003a7-109">Ehhez a parancshoz nem hozható létre új integrációs fiók.</span><span class="sxs-lookup"><span data-stu-id="003a7-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="003a7-110">Ha a dinamikus paramétereket szeretné használni, csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzéséhez, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="003a7-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="003a7-111">Ha kihagy egy szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="003a7-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="003a7-112">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="003a7-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="003a7-113">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="003a7-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="003a7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="003a7-114">EXAMPLES</span></span>

### <span data-ttu-id="003a7-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="003a7-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="003a7-116">Ez a parancs frissíti az integrációs fiókot a X12-alapú hozzáférés-vezérlési számmal egy adott integrációs fiókhoz tartozó szerződéshez, és sikertelen az üzenet feldolgozási állapotát tartalmazó érték.</span><span class="sxs-lookup"><span data-stu-id="003a7-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="003a7-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="003a7-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="003a7-118">Ez a parancs frissíti az integrációs fiókot a EDIFACT-alapú hozzáférés-vezérlési számmal egy adott integrációs fiókhoz tartozó szerződéshez, és sikertelen az üzenet feldolgozási állapotát tartalmazó érték.</span><span class="sxs-lookup"><span data-stu-id="003a7-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="003a7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="003a7-119">PARAMETERS</span></span>

### <span data-ttu-id="003a7-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="003a7-120">-AgreementName</span></span>
<span data-ttu-id="003a7-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="003a7-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="003a7-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="003a7-122">-AgreementType</span></span>
<span data-ttu-id="003a7-123">Az integrációs fiókra vonatkozó szerződés típusa (X12 vagy EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="003a7-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="003a7-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="003a7-124">-ControlNumberValue</span></span>
<span data-ttu-id="003a7-125">Az integrációs fiók vezérlőelemének számértéke.</span><span class="sxs-lookup"><span data-stu-id="003a7-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="003a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003a7-126">-DefaultProfile</span></span>
<span data-ttu-id="003a7-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="003a7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003a7-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="003a7-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="003a7-129">A beérkezett üzenet feldolgozási állapota</span><span class="sxs-lookup"><span data-stu-id="003a7-129">The received message processing status.</span></span>

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

### <span data-ttu-id="003a7-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="003a7-130">-Name</span></span>
<span data-ttu-id="003a7-131">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="003a7-131">The integration account name.</span></span>

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

### <span data-ttu-id="003a7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003a7-132">-ResourceGroupName</span></span>
<span data-ttu-id="003a7-133">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="003a7-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="003a7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="003a7-134">-Confirm</span></span>
<span data-ttu-id="003a7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="003a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="003a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003a7-136">-WhatIf</span></span>
<span data-ttu-id="003a7-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="003a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003a7-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="003a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="003a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003a7-139">CommonParameters</span></span>
<span data-ttu-id="003a7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="003a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003a7-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003a7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003a7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="003a7-142">INPUTS</span></span>

### <span data-ttu-id="003a7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="003a7-143">System.String</span></span>

## <span data-ttu-id="003a7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="003a7-144">OUTPUTS</span></span>

### <span data-ttu-id="003a7-145">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="003a7-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="003a7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="003a7-146">NOTES</span></span>

## <span data-ttu-id="003a7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="003a7-147">RELATED LINKS</span></span>

<span data-ttu-id="003a7-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="003a7-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
