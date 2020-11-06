---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: bfbcfe06acbfefefcd754a7ad541ebafe31bae7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501788"
---
# <span data-ttu-id="716db-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="716db-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="716db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="716db-102">SYNOPSIS</span></span>
<span data-ttu-id="716db-103">Módosítja az integrációs fiókra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="716db-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="716db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="716db-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="716db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="716db-105">DESCRIPTION</span></span>
<span data-ttu-id="716db-106">A **set-AzureRmIntegrationAccountAgreement** parancsmag módosította az integrációs fiókokra vonatkozó szerződést.</span><span class="sxs-lookup"><span data-stu-id="716db-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="716db-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók szerződését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="716db-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="716db-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="716db-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="716db-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="716db-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="716db-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="716db-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="716db-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="716db-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="716db-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="716db-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="716db-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="716db-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="716db-114">Példák</span><span class="sxs-lookup"><span data-stu-id="716db-114">EXAMPLES</span></span>

### <span data-ttu-id="716db-115">1. példa: az integrációs fiókra vonatkozó szerződés frissítése</span><span class="sxs-lookup"><span data-stu-id="716db-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="716db-116">Ez a parancs frissíti az integrációs fiókot a megadott Azure Resource csoportban.</span><span class="sxs-lookup"><span data-stu-id="716db-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="716db-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="716db-117">PARAMETERS</span></span>

### <span data-ttu-id="716db-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="716db-118">-AgreementContent</span></span>
<span data-ttu-id="716db-119">A szerződés tartalmának meghatározása a JavaScript-objektum formátumban (JSON)</span><span class="sxs-lookup"><span data-stu-id="716db-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="716db-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="716db-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="716db-121">A szerződés tartalmának elérési útvonalát adja meg a szerződéshez.</span><span class="sxs-lookup"><span data-stu-id="716db-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="716db-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="716db-122">-AgreementName</span></span>
<span data-ttu-id="716db-123">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="716db-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="716db-124">-AgreementType</span></span>
<span data-ttu-id="716db-125">Az integrációs fiókra vonatkozó szerződés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="716db-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="716db-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="716db-127">X12</span><span class="sxs-lookup"><span data-stu-id="716db-127">X12</span></span> 
- <span data-ttu-id="716db-128">AS2</span><span class="sxs-lookup"><span data-stu-id="716db-128">AS2</span></span>
- <span data-ttu-id="716db-129">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="716db-129">Edifact</span></span>

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

### <span data-ttu-id="716db-130">-Force</span><span class="sxs-lookup"><span data-stu-id="716db-130">-Force</span></span>
<span data-ttu-id="716db-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="716db-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="716db-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="716db-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="716db-133">A vendégek számára a name Business Identity minősítőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="716db-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="716db-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="716db-135">Az integrációs fiókról szóló szerződés Guest Identity minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="716db-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="716db-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="716db-136">-GuestPartner</span></span>
<span data-ttu-id="716db-137">A vendég partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="716db-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="716db-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="716db-139">A Host partner Name Business Identity minősítőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="716db-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="716db-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="716db-141">Az integrációs fiók – szolgáltatói azonosító minősítő értéke.</span><span class="sxs-lookup"><span data-stu-id="716db-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="716db-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="716db-142">-HostPartner</span></span>
<span data-ttu-id="716db-143">A fogadó partner nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="716db-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="716db-144">-Metadata</span></span>
<span data-ttu-id="716db-145">A szerződés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="716db-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="716db-146">-Name</span></span>
<span data-ttu-id="716db-147">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-147">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="716db-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716db-148">-ResourceGroupName</span></span>
<span data-ttu-id="716db-149">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="716db-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="716db-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="716db-150">-Confirm</span></span>
<span data-ttu-id="716db-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="716db-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716db-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716db-152">-WhatIf</span></span>
<span data-ttu-id="716db-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="716db-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716db-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="716db-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716db-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716db-155">-DefaultProfile</span></span>
<span data-ttu-id="716db-156">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="716db-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716db-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716db-157">CommonParameters</span></span>
<span data-ttu-id="716db-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="716db-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716db-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716db-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716db-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="716db-160">INPUTS</span></span>

## <span data-ttu-id="716db-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="716db-161">OUTPUTS</span></span>

### <span data-ttu-id="716db-162">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="716db-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="716db-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="716db-163">NOTES</span></span>

## <span data-ttu-id="716db-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="716db-164">RELATED LINKS</span></span>

[<span data-ttu-id="716db-165">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="716db-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="716db-166">Új – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="716db-166">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="716db-167">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="716db-167">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


