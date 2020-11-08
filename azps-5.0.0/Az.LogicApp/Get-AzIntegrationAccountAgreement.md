---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187713"
---
# <span data-ttu-id="cf8ae-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf8ae-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cf8ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8ae-103">Megkapja az integrációs fiók szerződését.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="cf8ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf8ae-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8ae-106">A **Get-AzIntegrationAccountAgreement** parancsmag az adatintegrációs fiókokat egy Azure-erőforráscsoport alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="cf8ae-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="cf8ae-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cf8ae-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cf8ae-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cf8ae-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cf8ae-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cf8ae-112">EXAMPLES</span></span>

### <span data-ttu-id="cf8ae-113">Példa 1: integrációs fiókról szóló szerződés beszerzése</span><span class="sxs-lookup"><span data-stu-id="cf8ae-113">Example 1: Get an integration account agreement</span></span>
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

<span data-ttu-id="cf8ae-114">Ez a parancs a IntegrationAccountAgreement06 nevű integrációs fiókról szóló szerződést kap.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="cf8ae-115">2. példa: az integrációs fiókokra vonatkozó megállapodások beszerzése erőforráscsoport nevével</span><span class="sxs-lookup"><span data-stu-id="cf8ae-115">Example 2: Get integration account agreements by resource group name</span></span>
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

<span data-ttu-id="cf8ae-116">Ez a parancs az integrációs fiókokra vonatkozó szerződéseket az erőforráscsoport neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="cf8ae-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf8ae-117">PARAMETERS</span></span>

### <span data-ttu-id="cf8ae-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="cf8ae-118">-AgreementName</span></span>
<span data-ttu-id="cf8ae-119">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="cf8ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8ae-120">-DefaultProfile</span></span>
<span data-ttu-id="cf8ae-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cf8ae-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf8ae-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf8ae-122">-Name</span></span>
<span data-ttu-id="cf8ae-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cf8ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf8ae-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf8ae-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cf8ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8ae-126">CommonParameters</span></span>
<span data-ttu-id="cf8ae-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf8ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8ae-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf8ae-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8ae-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf8ae-129">INPUTS</span></span>

### <span data-ttu-id="cf8ae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cf8ae-130">System.String</span></span>

## <span data-ttu-id="cf8ae-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf8ae-131">OUTPUTS</span></span>

### <span data-ttu-id="cf8ae-132">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf8ae-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="cf8ae-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf8ae-133">NOTES</span></span>

## <span data-ttu-id="cf8ae-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf8ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf8ae-135">Új – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf8ae-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cf8ae-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf8ae-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cf8ae-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf8ae-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


