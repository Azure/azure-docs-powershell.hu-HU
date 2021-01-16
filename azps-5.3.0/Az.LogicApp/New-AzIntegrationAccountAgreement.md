---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480210"
---
# <span data-ttu-id="a8479-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a8479-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="a8479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8479-102">SYNOPSIS</span></span>
<span data-ttu-id="a8479-103">Létrehoz egy integrációs fiókszerződést.</span><span class="sxs-lookup"><span data-stu-id="a8479-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="a8479-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8479-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8479-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8479-105">DESCRIPTION</span></span>
<span data-ttu-id="a8479-106">A **New-AzIntegrationAccountAgreement** parancsmag létrehoz egy integrációs fiókszerződést.</span><span class="sxs-lookup"><span data-stu-id="a8479-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="a8479-107">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiókszerződést képviseli.</span><span class="sxs-lookup"><span data-stu-id="a8479-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="a8479-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét, a szerződés nevét, a típust, a partner nevét, a partner minősítőit és a szerződés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="a8479-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="a8479-109">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterobjektumában megadott paraméterértékekkel.</span><span class="sxs-lookup"><span data-stu-id="a8479-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="a8479-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a8479-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a8479-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="a8479-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a8479-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="a8479-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a8479-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="a8479-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a8479-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8479-114">EXAMPLES</span></span>

### <span data-ttu-id="a8479-115">1. példa: Integrációs fiókszerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="a8479-115">Example 1: Create a integration account agreement</span></span>
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

<span data-ttu-id="a8479-116">Ez a parancs egy integrációs fiókszerződést hoz létre a megadott Azure-erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="a8479-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="a8479-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="a8479-117">Example 2</span></span>

<span data-ttu-id="a8479-118">Létrehoz egy integrációs fiókszerződést.</span><span class="sxs-lookup"><span data-stu-id="a8479-118">Creates an integration account agreement.</span></span> <span data-ttu-id="a8479-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="a8479-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="a8479-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8479-120">PARAMETERS</span></span>

### <span data-ttu-id="a8479-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="a8479-121">-AgreementContent</span></span>
<span data-ttu-id="a8479-122">A szerződés tartalmát adja meg JavaScript Object Notation (JSON) formátumban a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="a8479-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="a8479-123">Adja meg ezt a paramétert vagy *a AgreementContentFilePath paramétert.*</span><span class="sxs-lookup"><span data-stu-id="a8479-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="a8479-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="a8479-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="a8479-125">A szerződés tartalmának fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="a8479-126">Adja meg ezt a paramétert vagy *a AgreementContent paramétert.*</span><span class="sxs-lookup"><span data-stu-id="a8479-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="a8479-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a8479-127">-AgreementName</span></span>
<span data-ttu-id="a8479-128">Megadja az integrációs fiókszerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="a8479-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="a8479-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="a8479-129">-AgreementType</span></span>
<span data-ttu-id="a8479-130">Az integrációs fiók szerződéstípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="a8479-131">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a8479-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8479-132">X12</span><span class="sxs-lookup"><span data-stu-id="a8479-132">X12</span></span> 
- <span data-ttu-id="a8479-133">AS2</span><span class="sxs-lookup"><span data-stu-id="a8479-133">AS2</span></span>
- <span data-ttu-id="a8479-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="a8479-134">Edifact</span></span>

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

### <span data-ttu-id="a8479-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8479-135">-DefaultProfile</span></span>
<span data-ttu-id="a8479-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8479-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8479-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="a8479-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="a8479-138">Megadja a vendégpartnerhez tartozó név-üzleti identitás-törlőt.</span><span class="sxs-lookup"><span data-stu-id="a8479-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="a8479-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="a8479-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="a8479-140">Az integrációs fiók szerződésének vendég identitás-törlő értéke.</span><span class="sxs-lookup"><span data-stu-id="a8479-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="a8479-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="a8479-141">-GuestPartner</span></span>
<span data-ttu-id="a8479-142">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="a8479-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="a8479-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="a8479-144">Megadja a gazdapartnerhez tartozó név-üzleti identitás-törlőt.</span><span class="sxs-lookup"><span data-stu-id="a8479-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="a8479-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="a8479-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="a8479-146">Az integrációs fiókszerződés állomás identitás-törlő értéke.</span><span class="sxs-lookup"><span data-stu-id="a8479-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="a8479-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="a8479-147">-HostPartner</span></span>
<span data-ttu-id="a8479-148">A gazdapartner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="a8479-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a8479-149">-Metadata</span></span>
<span data-ttu-id="a8479-150">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="a8479-151">-Name</span><span class="sxs-lookup"><span data-stu-id="a8479-151">-Name</span></span>
<span data-ttu-id="a8479-152">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="a8479-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8479-153">-ResourceGroupName</span></span>
<span data-ttu-id="a8479-154">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8479-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a8479-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8479-155">-Confirm</span></span>
<span data-ttu-id="a8479-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a8479-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8479-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8479-157">-WhatIf</span></span>
<span data-ttu-id="a8479-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a8479-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8479-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8479-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8479-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8479-160">CommonParameters</span></span>
<span data-ttu-id="a8479-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8479-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8479-162">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8479-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8479-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8479-163">INPUTS</span></span>

### <span data-ttu-id="a8479-164">System.String</span><span class="sxs-lookup"><span data-stu-id="a8479-164">System.String</span></span>

## <span data-ttu-id="a8479-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8479-165">OUTPUTS</span></span>

### <span data-ttu-id="a8479-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a8479-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="a8479-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8479-167">NOTES</span></span>

## <span data-ttu-id="a8479-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8479-168">RELATED LINKS</span></span>

[<span data-ttu-id="a8479-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a8479-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="a8479-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a8479-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="a8479-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a8479-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


