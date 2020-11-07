---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 10cd1993acccf45e39a1b192f44b715b06f6d1d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835465"
---
# <span data-ttu-id="09bf7-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09bf7-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="09bf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="09bf7-103">Az integrációs fiókot létrehozó szerződés létrehozása.</span><span class="sxs-lookup"><span data-stu-id="09bf7-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="09bf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09bf7-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09bf7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="09bf7-106">A **New-AzIntegrationAccountAgreement** parancsmag létrehoz egy integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="09bf7-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="09bf7-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók szerződését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="09bf7-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="09bf7-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét, a szerződés nevét, a partner nevét, a partner-minősítőket és a szerződés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="09bf7-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="09bf7-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="09bf7-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="09bf7-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="09bf7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09bf7-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="09bf7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09bf7-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="09bf7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09bf7-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="09bf7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="09bf7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="09bf7-114">EXAMPLES</span></span>

### <span data-ttu-id="09bf7-115">1. példa: az integrációs fiókra vonatkozó szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="09bf7-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="09bf7-116">Ez a parancs létrehoz egy integrációs fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="09bf7-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="09bf7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09bf7-117">PARAMETERS</span></span>

### <span data-ttu-id="09bf7-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="09bf7-118">-AgreementContent</span></span>
<span data-ttu-id="09bf7-119">A szerződés tartalmának meghatározása a JavaScript-objektum formátumban (JSON)</span><span class="sxs-lookup"><span data-stu-id="09bf7-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="09bf7-120">Adja meg ezt a paramétert vagy a *AgreementContentFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="09bf7-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bf7-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="09bf7-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="09bf7-122">A szerződés tartalmának elérési útvonalát adja meg a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="09bf7-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="09bf7-123">Adja meg ezt a paramétert vagy a *AgreementContent* paramétert.</span><span class="sxs-lookup"><span data-stu-id="09bf7-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bf7-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="09bf7-124">-AgreementName</span></span>
<span data-ttu-id="09bf7-125">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="09bf7-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="09bf7-126">-AgreementType</span></span>
<span data-ttu-id="09bf7-127">Az integrációs fiókra vonatkozó szerződés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="09bf7-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="09bf7-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09bf7-129">X12</span><span class="sxs-lookup"><span data-stu-id="09bf7-129">X12</span></span> 
- <span data-ttu-id="09bf7-130">AS2</span><span class="sxs-lookup"><span data-stu-id="09bf7-130">AS2</span></span>
- <span data-ttu-id="09bf7-131">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="09bf7-131">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bf7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bf7-132">-DefaultProfile</span></span>
<span data-ttu-id="09bf7-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="09bf7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09bf7-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="09bf7-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="09bf7-135">A vendégek számára a name Business Identity minősítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="09bf7-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="09bf7-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="09bf7-137">Az integrációs fiókról szóló szerződés Guest Identity minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="09bf7-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="09bf7-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="09bf7-138">-GuestPartner</span></span>
<span data-ttu-id="09bf7-139">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="09bf7-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="09bf7-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="09bf7-141">A Host partner Name Business Identity minősítőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="09bf7-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="09bf7-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="09bf7-143">Az integrációs fiók – szolgáltatói azonosító minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="09bf7-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="09bf7-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="09bf7-144">-HostPartner</span></span>
<span data-ttu-id="09bf7-145">A fogadó partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="09bf7-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="09bf7-146">-Metadata</span></span>
<span data-ttu-id="09bf7-147">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bf7-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09bf7-148">-Name</span></span>
<span data-ttu-id="09bf7-149">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-149">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bf7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09bf7-150">-ResourceGroupName</span></span>
<span data-ttu-id="09bf7-151">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09bf7-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09bf7-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09bf7-152">-Confirm</span></span>
<span data-ttu-id="09bf7-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09bf7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09bf7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09bf7-154">-WhatIf</span></span>
<span data-ttu-id="09bf7-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09bf7-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09bf7-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09bf7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09bf7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bf7-157">CommonParameters</span></span>
<span data-ttu-id="09bf7-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09bf7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bf7-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09bf7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bf7-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09bf7-160">INPUTS</span></span>

### <span data-ttu-id="09bf7-161">System. String</span><span class="sxs-lookup"><span data-stu-id="09bf7-161">System.String</span></span>

## <span data-ttu-id="09bf7-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09bf7-162">OUTPUTS</span></span>

### <span data-ttu-id="09bf7-163">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09bf7-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="09bf7-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09bf7-164">NOTES</span></span>

## <span data-ttu-id="09bf7-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09bf7-165">RELATED LINKS</span></span>

[<span data-ttu-id="09bf7-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09bf7-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="09bf7-167">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09bf7-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="09bf7-168">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09bf7-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


