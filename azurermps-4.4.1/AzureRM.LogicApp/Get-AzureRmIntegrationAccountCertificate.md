---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 3d26bca20befc31edfa437c7d3f9bc5dfced2b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493475"
---
# <span data-ttu-id="c7b00-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b00-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="c7b00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7b00-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b00-103">Az integrációs fiók tanúsítványait egy erőforráscsoport kapja.</span><span class="sxs-lookup"><span data-stu-id="c7b00-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7b00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7b00-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7b00-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7b00-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b00-106">A **Get-AzureRmIntegrationAccountCertificate** parancsmag egy erőforráscsoport integrációs fiókjának tanúsítványait kapja.</span><span class="sxs-lookup"><span data-stu-id="c7b00-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="c7b00-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="c7b00-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="c7b00-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c7b00-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c7b00-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c7b00-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c7b00-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7b00-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c7b00-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c7b00-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c7b00-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c7b00-112">EXAMPLES</span></span>

### <span data-ttu-id="c7b00-113">Példa 1: integrációs fiók tanúsítványának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c7b00-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="c7b00-114">Ez a parancs a IntegrationAccountCertificate01 nevű integrációs fiók tanúsítványát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7b00-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="c7b00-115">2. példa: az integrációs fiók tanúsítványának beszerzése az integrációs fiók nevével</span><span class="sxs-lookup"><span data-stu-id="c7b00-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="c7b00-116">Ez a parancs a IntegrationAccount31 nevű integrációs fiókhoz tartozó integrációs fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7b00-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="c7b00-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7b00-117">PARAMETERS</span></span>

### <span data-ttu-id="c7b00-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c7b00-118">-CertificateName</span></span>
<span data-ttu-id="c7b00-119">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7b00-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="c7b00-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7b00-120">-Name</span></span>
<span data-ttu-id="c7b00-121">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7b00-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c7b00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b00-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7b00-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7b00-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7b00-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b00-124">-DefaultProfile</span></span>
<span data-ttu-id="c7b00-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7b00-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7b00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b00-126">CommonParameters</span></span>
<span data-ttu-id="c7b00-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7b00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b00-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b00-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b00-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7b00-129">INPUTS</span></span>

## <span data-ttu-id="c7b00-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7b00-130">OUTPUTS</span></span>

### <span data-ttu-id="c7b00-131">Microsoft. Azure. Management. Logic. models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b00-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="c7b00-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7b00-132">NOTES</span></span>

## <span data-ttu-id="c7b00-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7b00-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7b00-134">Új – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b00-134">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c7b00-135">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b00-135">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c7b00-136">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c7b00-136">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


