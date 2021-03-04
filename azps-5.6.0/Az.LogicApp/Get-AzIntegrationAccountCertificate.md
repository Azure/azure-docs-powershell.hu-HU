---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: caf016d1e1ad18aee1904e9b69ae9330a5f34557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922922"
---
# <span data-ttu-id="b957c-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b957c-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b957c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b957c-102">SYNOPSIS</span></span>
<span data-ttu-id="b957c-103">Integrációs fióktanúsítványokat kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="b957c-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="b957c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b957c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b957c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b957c-105">DESCRIPTION</span></span>
<span data-ttu-id="b957c-106">A **Get-AzIntegrationAccountCertificate parancsmag** integrációs fióktanúsítványokat kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="b957c-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="b957c-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="b957c-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="b957c-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b957c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b957c-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="b957c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b957c-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="b957c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b957c-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="b957c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b957c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b957c-112">EXAMPLES</span></span>

### <span data-ttu-id="b957c-113">1. példa: Integrációs fiók tanúsítványának létrehozása</span><span class="sxs-lookup"><span data-stu-id="b957c-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="b957c-114">Ez a parancs az IntegrationAccountCertificate01 nevű integrációs fiók tanúsítványát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b957c-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="b957c-115">2. példa: Integrációs fiók tanúsítványának lekérte az integrációs fiók neve alapján</span><span class="sxs-lookup"><span data-stu-id="b957c-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="b957c-116">Ez a parancs az IntegrationAccount31 nevű integrációs fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b957c-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="b957c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b957c-117">PARAMETERS</span></span>

### <span data-ttu-id="b957c-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b957c-118">-CertificateName</span></span>
<span data-ttu-id="b957c-119">Egy integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b957c-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="b957c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b957c-120">-DefaultProfile</span></span>
<span data-ttu-id="b957c-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b957c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b957c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b957c-122">-Name</span></span>
<span data-ttu-id="b957c-123">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b957c-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b957c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b957c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b957c-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b957c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b957c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b957c-126">CommonParameters</span></span>
<span data-ttu-id="b957c-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b957c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b957c-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b957c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b957c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b957c-129">INPUTS</span></span>

### <span data-ttu-id="b957c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b957c-130">System.String</span></span>

## <span data-ttu-id="b957c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b957c-131">OUTPUTS</span></span>

### <span data-ttu-id="b957c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b957c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="b957c-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b957c-133">NOTES</span></span>

## <span data-ttu-id="b957c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b957c-134">RELATED LINKS</span></span>

[<span data-ttu-id="b957c-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b957c-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b957c-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b957c-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b957c-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b957c-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


