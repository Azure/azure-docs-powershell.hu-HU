---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147643"
---
# <span data-ttu-id="bb652-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bb652-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="bb652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb652-102">SYNOPSIS</span></span>
<span data-ttu-id="bb652-103">Integrációs fióktanúsítványokat kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="bb652-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="bb652-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bb652-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb652-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bb652-105">DESCRIPTION</span></span>
<span data-ttu-id="bb652-106">A **Get-AzIntegrationAccountCertificate parancsmag** integrációs fióktanúsítványokat kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="bb652-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="bb652-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="bb652-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="bb652-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="bb652-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bb652-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="bb652-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bb652-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="bb652-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bb652-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="bb652-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bb652-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bb652-112">EXAMPLES</span></span>

### <span data-ttu-id="bb652-113">1. példa: Integrációs fiók tanúsítványának létrehozása</span><span class="sxs-lookup"><span data-stu-id="bb652-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="bb652-114">Ez a parancs az IntegrationAccountCertificate01 nevű integrációs fiók tanúsítványát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bb652-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="bb652-115">2. példa: Integrációs fióktanúsítványok lekérte az integrációs fiók neve alapján</span><span class="sxs-lookup"><span data-stu-id="bb652-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="bb652-116">Ez a parancs az IntegrationAccount31 nevű integrációs fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bb652-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="bb652-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb652-117">PARAMETERS</span></span>

### <span data-ttu-id="bb652-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bb652-118">-CertificateName</span></span>
<span data-ttu-id="bb652-119">Egy integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb652-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="bb652-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb652-120">-DefaultProfile</span></span>
<span data-ttu-id="bb652-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb652-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb652-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb652-122">-Name</span></span>
<span data-ttu-id="bb652-123">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb652-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="bb652-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb652-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb652-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb652-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bb652-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb652-126">CommonParameters</span></span>
<span data-ttu-id="bb652-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb652-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb652-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb652-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb652-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb652-129">INPUTS</span></span>

### <span data-ttu-id="bb652-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bb652-130">System.String</span></span>

## <span data-ttu-id="bb652-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb652-131">OUTPUTS</span></span>

### <span data-ttu-id="bb652-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bb652-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="bb652-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bb652-133">NOTES</span></span>

## <span data-ttu-id="bb652-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb652-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb652-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bb652-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="bb652-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bb652-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="bb652-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bb652-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


