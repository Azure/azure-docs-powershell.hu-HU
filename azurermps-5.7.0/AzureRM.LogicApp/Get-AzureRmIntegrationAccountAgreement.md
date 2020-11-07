---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: eadd3052bb965b60bdaf377cd45fc014f25cac79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678983"
---
# <span data-ttu-id="73205-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73205-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="73205-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73205-102">SYNOPSIS</span></span>
<span data-ttu-id="73205-103">Megkapja az integrációs fiók szerződését.</span><span class="sxs-lookup"><span data-stu-id="73205-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73205-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73205-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73205-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73205-105">DESCRIPTION</span></span>
<span data-ttu-id="73205-106">A **Get-AzureRmIntegrationAccountAgreement** parancsmag az adatintegrációs fiókokat egy Azure-erőforráscsoport alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="73205-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="73205-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a szerződés nevét.</span><span class="sxs-lookup"><span data-stu-id="73205-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="73205-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="73205-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73205-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="73205-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73205-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="73205-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73205-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="73205-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73205-112">Példák</span><span class="sxs-lookup"><span data-stu-id="73205-112">EXAMPLES</span></span>

### <span data-ttu-id="73205-113">Példa 1: integrációs fiókról szóló szerződés beszerzése</span><span class="sxs-lookup"><span data-stu-id="73205-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="73205-114">Ez a parancs a IntegrationAccountAgreement06 nevű integrációs fiókról szóló szerződést kap.</span><span class="sxs-lookup"><span data-stu-id="73205-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="73205-115">2. példa: az integrációs fiókokra vonatkozó megállapodások beszerzése erőforráscsoport nevével</span><span class="sxs-lookup"><span data-stu-id="73205-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="73205-116">Ez a parancs az integrációs fiókokra vonatkozó szerződéseket az erőforráscsoport neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="73205-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="73205-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73205-117">PARAMETERS</span></span>

### <span data-ttu-id="73205-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="73205-118">-AgreementName</span></span>
<span data-ttu-id="73205-119">Az integrációs fiókra vonatkozó szerződés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73205-119">Specifies the name of an integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73205-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73205-120">-DefaultProfile</span></span>
<span data-ttu-id="73205-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="73205-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73205-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73205-122">-Name</span></span>
<span data-ttu-id="73205-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73205-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73205-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73205-124">-ResourceGroupName</span></span>
<span data-ttu-id="73205-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73205-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73205-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73205-126">CommonParameters</span></span>
<span data-ttu-id="73205-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73205-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73205-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73205-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73205-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73205-129">INPUTS</span></span>

### <span data-ttu-id="73205-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="73205-130">None</span></span>
<span data-ttu-id="73205-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="73205-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73205-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73205-132">OUTPUTS</span></span>

### <span data-ttu-id="73205-133">Microsoft. Azure. Management. Logic. models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73205-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="73205-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73205-134">NOTES</span></span>

## <span data-ttu-id="73205-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73205-135">RELATED LINKS</span></span>

[<span data-ttu-id="73205-136">Új – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73205-136">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="73205-137">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73205-137">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="73205-138">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73205-138">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


