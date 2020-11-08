---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025285"
---
# <span data-ttu-id="d4184-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4184-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="d4184-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4184-102">SYNOPSIS</span></span>
<span data-ttu-id="d4184-103">Az integrációs fiókot létrehozó szerződés létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d4184-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="d4184-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4184-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4184-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4184-105">DESCRIPTION</span></span>
<span data-ttu-id="d4184-106">A **New-AzIntegrationAccountAgreement** parancsmag létrehoz egy integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="d4184-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="d4184-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók szerződését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d4184-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="d4184-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét, a szerződés nevét, a partner nevét, a partner-minősítőket és a szerződés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="d4184-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="d4184-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="d4184-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d4184-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d4184-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d4184-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d4184-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d4184-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="d4184-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4184-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="d4184-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4184-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d4184-114">EXAMPLES</span></span>

### <span data-ttu-id="d4184-115">1. példa: az integrációs fiókra vonatkozó szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="d4184-115">Example 1: Create a integration account agreement</span></span>
```powershell
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

<span data-ttu-id="d4184-116">Ez a parancs létrehoz egy integrációs fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="d4184-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="d4184-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4184-117">Example 2</span></span>

<span data-ttu-id="d4184-118">Az integrációs fiókot létrehozó szerződés létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d4184-118">Creates an integration account agreement.</span></span> <span data-ttu-id="d4184-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="d4184-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="d4184-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4184-120">PARAMETERS</span></span>

### <span data-ttu-id="d4184-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="d4184-121">-AgreementContent</span></span>
<span data-ttu-id="d4184-122">A szerződés tartalmának meghatározása a JavaScript-objektum formátumban (JSON)</span><span class="sxs-lookup"><span data-stu-id="d4184-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="d4184-123">Adja meg ezt a paramétert vagy a *AgreementContentFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4184-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="d4184-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="d4184-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="d4184-125">A szerződés tartalmának elérési útvonalát adja meg a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="d4184-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="d4184-126">Adja meg ezt a paramétert vagy a *AgreementContent* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4184-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="d4184-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d4184-127">-AgreementName</span></span>
<span data-ttu-id="d4184-128">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="d4184-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d4184-129">-AgreementType</span></span>
<span data-ttu-id="d4184-130">Az integrációs fiókra vonatkozó szerződés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="d4184-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d4184-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4184-132">X12</span><span class="sxs-lookup"><span data-stu-id="d4184-132">X12</span></span> 
- <span data-ttu-id="d4184-133">AS2</span><span class="sxs-lookup"><span data-stu-id="d4184-133">AS2</span></span>
- <span data-ttu-id="d4184-134">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="d4184-134">Edifact</span></span>

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

### <span data-ttu-id="d4184-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4184-135">-DefaultProfile</span></span>
<span data-ttu-id="d4184-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4184-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4184-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d4184-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="d4184-138">A vendégek számára a name Business Identity minősítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="d4184-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d4184-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="d4184-140">Az integrációs fiókról szóló szerződés Guest Identity minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="d4184-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="d4184-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="d4184-141">-GuestPartner</span></span>
<span data-ttu-id="d4184-142">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="d4184-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d4184-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="d4184-144">A Host partner Name Business Identity minősítőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="d4184-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d4184-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="d4184-146">Az integrációs fiók – szolgáltatói azonosító minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="d4184-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="d4184-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="d4184-147">-HostPartner</span></span>
<span data-ttu-id="d4184-148">A fogadó partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="d4184-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d4184-149">-Metadata</span></span>
<span data-ttu-id="d4184-150">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="d4184-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4184-151">-Name</span></span>
<span data-ttu-id="d4184-152">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d4184-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4184-153">-ResourceGroupName</span></span>
<span data-ttu-id="d4184-154">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4184-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4184-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4184-155">-Confirm</span></span>
<span data-ttu-id="d4184-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4184-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4184-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4184-157">-WhatIf</span></span>
<span data-ttu-id="d4184-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4184-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4184-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4184-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4184-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4184-160">CommonParameters</span></span>
<span data-ttu-id="d4184-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4184-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4184-162">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4184-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4184-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4184-163">INPUTS</span></span>

### <span data-ttu-id="d4184-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d4184-164">System.String</span></span>

## <span data-ttu-id="d4184-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4184-165">OUTPUTS</span></span>

### <span data-ttu-id="d4184-166">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4184-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="d4184-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4184-167">NOTES</span></span>

## <span data-ttu-id="d4184-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4184-168">RELATED LINKS</span></span>

[<span data-ttu-id="d4184-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4184-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d4184-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4184-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d4184-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d4184-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


