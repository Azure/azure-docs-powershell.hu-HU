---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 268dd2c54d9881281a5b1ee331a5b5d98892f7b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500560"
---
# <span data-ttu-id="4f26e-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f26e-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="4f26e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f26e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f26e-103">Az integrációs fiók tanúsítványait egy erőforráscsoport kapja.</span><span class="sxs-lookup"><span data-stu-id="4f26e-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f26e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f26e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f26e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f26e-105">DESCRIPTION</span></span>
<span data-ttu-id="4f26e-106">A **Get-AzureRmIntegrationAccountCertificate** parancsmag egy erőforráscsoport integrációs fiókjának tanúsítványait kapja.</span><span class="sxs-lookup"><span data-stu-id="4f26e-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="4f26e-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="4f26e-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="4f26e-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="4f26e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f26e-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="4f26e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f26e-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="4f26e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f26e-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="4f26e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4f26e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4f26e-112">EXAMPLES</span></span>

### <span data-ttu-id="4f26e-113">Példa 1: integrációs fiók tanúsítványának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4f26e-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4f26e-114">Ez a parancs a IntegrationAccountCertificate01 nevű integrációs fiók tanúsítványát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4f26e-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="4f26e-115">2. példa: az integrációs fiók tanúsítványának beszerzése az integrációs fiók nevével</span><span class="sxs-lookup"><span data-stu-id="4f26e-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4f26e-116">Ez a parancs a IntegrationAccount31 nevű integrációs fiókhoz tartozó integrációs fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4f26e-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="4f26e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f26e-117">PARAMETERS</span></span>

### <span data-ttu-id="4f26e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4f26e-118">-CertificateName</span></span>
<span data-ttu-id="4f26e-119">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f26e-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="4f26e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f26e-120">-DefaultProfile</span></span>
<span data-ttu-id="4f26e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f26e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f26e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4f26e-122">-Name</span></span>
<span data-ttu-id="4f26e-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f26e-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="4f26e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f26e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f26e-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f26e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f26e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f26e-126">CommonParameters</span></span>
<span data-ttu-id="4f26e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f26e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f26e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f26e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f26e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f26e-129">INPUTS</span></span>

### <span data-ttu-id="4f26e-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="4f26e-130">None</span></span>
<span data-ttu-id="4f26e-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4f26e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f26e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f26e-132">OUTPUTS</span></span>

### <span data-ttu-id="4f26e-133">Microsoft. Azure. Management. Logic. models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f26e-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="4f26e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f26e-134">NOTES</span></span>

## <span data-ttu-id="4f26e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f26e-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f26e-136">Új – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f26e-136">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4f26e-137">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f26e-137">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4f26e-138">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f26e-138">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


