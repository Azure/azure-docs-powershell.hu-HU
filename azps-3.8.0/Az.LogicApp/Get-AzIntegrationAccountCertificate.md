---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846002"
---
# <span data-ttu-id="99791-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="99791-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="99791-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99791-102">SYNOPSIS</span></span>
<span data-ttu-id="99791-103">Az integrációs fiók tanúsítványait egy erőforráscsoport kapja.</span><span class="sxs-lookup"><span data-stu-id="99791-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="99791-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99791-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99791-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99791-105">DESCRIPTION</span></span>
<span data-ttu-id="99791-106">A **Get-AzIntegrationAccountCertificate** parancsmag egy erőforráscsoport integrációs fiókjának tanúsítványait kapja.</span><span class="sxs-lookup"><span data-stu-id="99791-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="99791-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="99791-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="99791-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="99791-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="99791-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="99791-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="99791-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="99791-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="99791-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="99791-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="99791-112">Példák</span><span class="sxs-lookup"><span data-stu-id="99791-112">EXAMPLES</span></span>

### <span data-ttu-id="99791-113">Példa 1: integrációs fiók tanúsítványának beszerzése</span><span class="sxs-lookup"><span data-stu-id="99791-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="99791-114">Ez a parancs a IntegrationAccountCertificate01 nevű integrációs fiók tanúsítványát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="99791-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="99791-115">2. példa: az integrációs fiók tanúsítványának beszerzése az integrációs fiók nevével</span><span class="sxs-lookup"><span data-stu-id="99791-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="99791-116">Ez a parancs a IntegrationAccount31 nevű integrációs fiókhoz tartozó integrációs fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="99791-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="99791-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99791-117">PARAMETERS</span></span>

### <span data-ttu-id="99791-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="99791-118">-CertificateName</span></span>
<span data-ttu-id="99791-119">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99791-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="99791-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99791-120">-DefaultProfile</span></span>
<span data-ttu-id="99791-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="99791-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99791-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99791-122">-Name</span></span>
<span data-ttu-id="99791-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99791-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="99791-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99791-124">-ResourceGroupName</span></span>
<span data-ttu-id="99791-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99791-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="99791-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99791-126">CommonParameters</span></span>
<span data-ttu-id="99791-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99791-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99791-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99791-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99791-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99791-129">INPUTS</span></span>

### <span data-ttu-id="99791-130">System. String</span><span class="sxs-lookup"><span data-stu-id="99791-130">System.String</span></span>

## <span data-ttu-id="99791-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99791-131">OUTPUTS</span></span>

### <span data-ttu-id="99791-132">Microsoft. Azure. Management. Logic. models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="99791-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="99791-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99791-133">NOTES</span></span>

## <span data-ttu-id="99791-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99791-134">RELATED LINKS</span></span>

[<span data-ttu-id="99791-135">Új – AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="99791-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="99791-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="99791-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="99791-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="99791-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


