---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 732c7cd1feb54c1475839a39f57f81d154da80ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492258"
---
# <span data-ttu-id="d2b0b-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d2b0b-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="d2b0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b0b-103">Frissíti az Adathozzáférési fiók által generált bankközi vezérlő számot (NVH) az Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2b0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2b0b-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2b0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b0b-106">A Set-AzureRmIntegrationAccountGeneratedIcn parancsmag egy meglévő, az integrációt szabályozó számot (NVH) frissít, és egy olyan objektumot ad eredményül, amely a bankközi vezérlő által generált integrációs fiókot képviseli.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="d2b0b-107">Ezzel a parancsmaggal frissítheti az adatintegrációs fiókok által generált bankközi vezérlő számát.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="d2b0b-108">Az integrációs fiókokat az integrációs fiók nevének, az erőforráscsoport nevének és a szerződés nevének megadásával frissítheti.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="d2b0b-109">Ehhez a parancshoz nem hozható létre új integrációs fiók.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="d2b0b-110">Ha a dinamikus paramétereket szeretné használni, csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzéséhez, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d2b0b-111">Ha kihagy egy szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="d2b0b-112">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d2b0b-113">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d2b0b-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d2b0b-114">EXAMPLES</span></span>

### <span data-ttu-id="d2b0b-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2b0b-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d2b0b-116">Ez a parancs beilleszti az integrációs fiókot, amely egy adott integrációs X12 generálta az adatcsere-vezérlési számot egy adott integrációs fiókra vonatkozó szerződéshez, az 100 értékét a módosított értékre</span><span class="sxs-lookup"><span data-stu-id="d2b0b-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="d2b0b-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="d2b0b-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d2b0b-118">Ez a parancs beilleszti az integrációs fiókot, amely egy adott integrációs EdifactIntegrationAccountAgreement generálta az adatcsere-vezérlési számot egy adott integrációs fiókra vonatkozó szerződéshez, az 100 értékét a módosított értékre</span><span class="sxs-lookup"><span data-stu-id="d2b0b-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="d2b0b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2b0b-119">PARAMETERS</span></span>

### <span data-ttu-id="d2b0b-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d2b0b-120">-AgreementName</span></span>
<span data-ttu-id="d2b0b-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-121">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d2b0b-122">-AgreementType</span></span>
<span data-ttu-id="d2b0b-123">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-123">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="d2b0b-124">-ControlNumber</span></span>
<span data-ttu-id="d2b0b-125">A generált vezérlőelem száma új érték.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-125">The generated control number new value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b0b-126">-DefaultProfile</span></span>
<span data-ttu-id="d2b0b-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2b0b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2b0b-128">-Name</span></span>
<span data-ttu-id="d2b0b-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-129">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2b0b-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2b0b-131">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-131">The integration account resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2b0b-132">-Confirm</span></span>
<span data-ttu-id="d2b0b-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b0b-134">-WhatIf</span></span>
<span data-ttu-id="d2b0b-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2b0b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2b0b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b0b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b0b-137">CommonParameters</span></span>
<span data-ttu-id="d2b0b-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2b0b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b0b-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b0b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b0b-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2b0b-140">INPUTS</span></span>

### <span data-ttu-id="d2b0b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d2b0b-141">System.String</span></span>

## <span data-ttu-id="d2b0b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2b0b-142">OUTPUTS</span></span>

### <span data-ttu-id="d2b0b-143">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="d2b0b-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="d2b0b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2b0b-144">NOTES</span></span>

## <span data-ttu-id="d2b0b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2b0b-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2b0b-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d2b0b-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

