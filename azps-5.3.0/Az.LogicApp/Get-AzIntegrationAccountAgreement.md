---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480078"
---
# <span data-ttu-id="99716-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="99716-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="99716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99716-102">SYNOPSIS</span></span>
<span data-ttu-id="99716-103">Integrációs fiókszerződést kap.</span><span class="sxs-lookup"><span data-stu-id="99716-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="99716-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99716-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99716-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99716-105">DESCRIPTION</span></span>
<span data-ttu-id="99716-106">A **Get-AzIntegrationAccountAgreement** parancsmag integrációs fiókszerződést kap egy Azure-erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="99716-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="99716-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="99716-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="99716-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="99716-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="99716-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="99716-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="99716-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="99716-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="99716-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="99716-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="99716-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99716-112">EXAMPLES</span></span>

### <span data-ttu-id="99716-113">1. példa: Integrációs fiókszerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="99716-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="99716-114">Ez a parancs egy IntegrationAccountAgreement06 nevű integrációs fiókszerződést kap.</span><span class="sxs-lookup"><span data-stu-id="99716-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="99716-115">2. példa: Integrációs fiókszerződések lekérte az erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="99716-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="99716-116">Ez a parancs az integrációs fiókszerződéseket az erőforráscsoport neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="99716-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="99716-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99716-117">PARAMETERS</span></span>

### <span data-ttu-id="99716-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="99716-118">-AgreementName</span></span>
<span data-ttu-id="99716-119">Egy integrációs fiókszerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99716-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="99716-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99716-120">-DefaultProfile</span></span>
<span data-ttu-id="99716-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="99716-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99716-122">-Name</span><span class="sxs-lookup"><span data-stu-id="99716-122">-Name</span></span>
<span data-ttu-id="99716-123">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99716-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99716-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99716-124">-ResourceGroupName</span></span>
<span data-ttu-id="99716-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99716-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99716-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99716-126">CommonParameters</span></span>
<span data-ttu-id="99716-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99716-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99716-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99716-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99716-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99716-129">INPUTS</span></span>

### <span data-ttu-id="99716-130">System.String</span><span class="sxs-lookup"><span data-stu-id="99716-130">System.String</span></span>

## <span data-ttu-id="99716-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99716-131">OUTPUTS</span></span>

### <span data-ttu-id="99716-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="99716-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="99716-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99716-133">NOTES</span></span>

## <span data-ttu-id="99716-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99716-134">RELATED LINKS</span></span>

[<span data-ttu-id="99716-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="99716-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="99716-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="99716-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="99716-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="99716-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


