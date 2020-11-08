---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194663"
---
# <span data-ttu-id="08649-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="08649-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="08649-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08649-102">SYNOPSIS</span></span>
<span data-ttu-id="08649-103">Módosítja az integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="08649-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="08649-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08649-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08649-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08649-105">DESCRIPTION</span></span>
<span data-ttu-id="08649-106">A **set-AzIntegrationAccountAgreement** parancsmag módosította az integrációs fiókokra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="08649-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="08649-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók szerződését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="08649-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="08649-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="08649-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="08649-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="08649-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="08649-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="08649-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="08649-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="08649-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="08649-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="08649-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="08649-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="08649-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="08649-114">Példák</span><span class="sxs-lookup"><span data-stu-id="08649-114">EXAMPLES</span></span>

### <span data-ttu-id="08649-115">1. példa: az integrációs fiókra vonatkozó szerződés frissítése</span><span class="sxs-lookup"><span data-stu-id="08649-115">Example 1: Update an integration account agreement</span></span>
```powershell
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

<span data-ttu-id="08649-116">Ez a parancs frissíti az integrációs fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="08649-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="08649-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="08649-117">Example 2</span></span>

<span data-ttu-id="08649-118">Módosítja az integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="08649-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="08649-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="08649-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="08649-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08649-120">PARAMETERS</span></span>

### <span data-ttu-id="08649-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="08649-121">-AgreementContent</span></span>
<span data-ttu-id="08649-122">A szerződés tartalmának meghatározása a JavaScript-objektum formátumban (JSON)</span><span class="sxs-lookup"><span data-stu-id="08649-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="08649-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="08649-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="08649-124">A szerződés tartalmának elérési útvonalát adja meg a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="08649-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="08649-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="08649-125">-AgreementName</span></span>
<span data-ttu-id="08649-126">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="08649-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="08649-127">-AgreementType</span></span>
<span data-ttu-id="08649-128">Az integrációs fiókra vonatkozó szerződés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="08649-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="08649-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08649-130">X12</span><span class="sxs-lookup"><span data-stu-id="08649-130">X12</span></span> 
- <span data-ttu-id="08649-131">AS2</span><span class="sxs-lookup"><span data-stu-id="08649-131">AS2</span></span>
- <span data-ttu-id="08649-132">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="08649-132">Edifact</span></span>

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

### <span data-ttu-id="08649-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08649-133">-DefaultProfile</span></span>
<span data-ttu-id="08649-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08649-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08649-135">-Force</span><span class="sxs-lookup"><span data-stu-id="08649-135">-Force</span></span>
<span data-ttu-id="08649-136">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="08649-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08649-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="08649-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="08649-138">A vendégek számára a name Business Identity minősítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="08649-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="08649-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="08649-140">Az integrációs fiókról szóló szerződés Guest Identity minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="08649-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="08649-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="08649-141">-GuestPartner</span></span>
<span data-ttu-id="08649-142">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="08649-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="08649-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="08649-144">A Host partner Name Business Identity minősítőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="08649-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="08649-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="08649-146">Az integrációs fiók – szolgáltatói azonosító minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="08649-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="08649-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="08649-147">-HostPartner</span></span>
<span data-ttu-id="08649-148">A fogadó partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="08649-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="08649-149">-Metadata</span></span>
<span data-ttu-id="08649-150">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="08649-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08649-151">-Name</span></span>
<span data-ttu-id="08649-152">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="08649-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08649-153">-ResourceGroupName</span></span>
<span data-ttu-id="08649-154">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08649-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08649-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08649-155">-Confirm</span></span>
<span data-ttu-id="08649-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08649-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08649-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08649-157">-WhatIf</span></span>
<span data-ttu-id="08649-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08649-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08649-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08649-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08649-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08649-160">CommonParameters</span></span>
<span data-ttu-id="08649-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08649-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08649-162">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08649-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08649-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08649-163">INPUTS</span></span>

### <span data-ttu-id="08649-164">System. String</span><span class="sxs-lookup"><span data-stu-id="08649-164">System.String</span></span>

## <span data-ttu-id="08649-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08649-165">OUTPUTS</span></span>

### <span data-ttu-id="08649-166">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="08649-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="08649-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08649-167">NOTES</span></span>

## <span data-ttu-id="08649-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08649-168">RELATED LINKS</span></span>

[<span data-ttu-id="08649-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="08649-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="08649-170">Új – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="08649-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="08649-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="08649-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


