---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: c69bee32a8a1f537f56f8268c4aedadce3174fdc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002885"
---
# <span data-ttu-id="98597-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="98597-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="98597-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98597-102">SYNOPSIS</span></span>
<span data-ttu-id="98597-103">Módosítja az integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="98597-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="98597-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98597-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98597-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98597-105">DESCRIPTION</span></span>
<span data-ttu-id="98597-106">A **set-AzIntegrationAccountAgreement** parancsmag módosította az integrációs fiókokra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="98597-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="98597-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók szerződését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="98597-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="98597-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="98597-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="98597-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="98597-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="98597-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="98597-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="98597-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="98597-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="98597-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="98597-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="98597-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="98597-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="98597-114">Példák</span><span class="sxs-lookup"><span data-stu-id="98597-114">EXAMPLES</span></span>

### <span data-ttu-id="98597-115">1. példa: az integrációs fiókra vonatkozó szerződés frissítése</span><span class="sxs-lookup"><span data-stu-id="98597-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="98597-116">Ez a parancs frissíti az integrációs fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="98597-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="98597-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98597-117">PARAMETERS</span></span>

### <span data-ttu-id="98597-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="98597-118">-AgreementContent</span></span>
<span data-ttu-id="98597-119">A szerződés tartalmának meghatározása a JavaScript-objektum formátumban (JSON)</span><span class="sxs-lookup"><span data-stu-id="98597-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="98597-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="98597-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="98597-121">A szerződés tartalmának elérési útvonalát adja meg a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="98597-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="98597-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="98597-122">-AgreementName</span></span>
<span data-ttu-id="98597-123">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="98597-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="98597-124">-AgreementType</span></span>
<span data-ttu-id="98597-125">Az integrációs fiókra vonatkozó szerződés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="98597-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98597-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98597-127">X12</span><span class="sxs-lookup"><span data-stu-id="98597-127">X12</span></span> 
- <span data-ttu-id="98597-128">AS2</span><span class="sxs-lookup"><span data-stu-id="98597-128">AS2</span></span>
- <span data-ttu-id="98597-129">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="98597-129">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98597-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98597-130">-DefaultProfile</span></span>
<span data-ttu-id="98597-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98597-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98597-132">-Force</span><span class="sxs-lookup"><span data-stu-id="98597-132">-Force</span></span>
<span data-ttu-id="98597-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="98597-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98597-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="98597-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="98597-135">A vendégek számára a name Business Identity minősítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="98597-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="98597-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="98597-137">Az integrációs fiókról szóló szerződés Guest Identity minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="98597-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="98597-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="98597-138">-GuestPartner</span></span>
<span data-ttu-id="98597-139">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="98597-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="98597-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="98597-141">A Host partner Name Business Identity minősítőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="98597-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="98597-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="98597-143">Az integrációs fiók – szolgáltatói azonosító minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="98597-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="98597-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="98597-144">-HostPartner</span></span>
<span data-ttu-id="98597-145">A fogadó partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="98597-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="98597-146">-Metadata</span></span>
<span data-ttu-id="98597-147">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="98597-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98597-148">-Name</span></span>
<span data-ttu-id="98597-149">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-149">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="98597-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98597-150">-ResourceGroupName</span></span>
<span data-ttu-id="98597-151">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98597-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="98597-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98597-152">-Confirm</span></span>
<span data-ttu-id="98597-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98597-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98597-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98597-154">-WhatIf</span></span>
<span data-ttu-id="98597-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98597-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98597-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98597-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98597-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98597-157">CommonParameters</span></span>
<span data-ttu-id="98597-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98597-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98597-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98597-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98597-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98597-160">INPUTS</span></span>

### <span data-ttu-id="98597-161">System. String</span><span class="sxs-lookup"><span data-stu-id="98597-161">System.String</span></span>

## <span data-ttu-id="98597-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98597-162">OUTPUTS</span></span>

### <span data-ttu-id="98597-163">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="98597-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="98597-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98597-164">NOTES</span></span>

## <span data-ttu-id="98597-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98597-165">RELATED LINKS</span></span>

[<span data-ttu-id="98597-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="98597-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="98597-167">Új – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="98597-167">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="98597-168">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="98597-168">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


