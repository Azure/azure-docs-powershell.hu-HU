---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184478"
---
# <span data-ttu-id="1b038-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1b038-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1b038-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b038-102">SYNOPSIS</span></span>
<span data-ttu-id="1b038-103">Létrehozza az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="1b038-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="1b038-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b038-104">SYNTAX</span></span>

### <span data-ttu-id="1b038-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="1b038-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b038-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="1b038-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b038-107">Mind</span><span class="sxs-lookup"><span data-stu-id="1b038-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b038-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b038-108">DESCRIPTION</span></span>
<span data-ttu-id="1b038-109">A **New-AzIntegrationAccountCertificate** parancsmag létrehozza az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="1b038-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="1b038-110">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók tanúsítványát képviseli.</span><span class="sxs-lookup"><span data-stu-id="1b038-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="1b038-111">Adja meg az integrációs fiók nevét, az erőforrás csoport nevét, a tanúsítvány nevét, a kulcs nevét, a kulcs verziószámát és a kulcsfájl AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="1b038-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="1b038-112">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="1b038-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1b038-113">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="1b038-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1b038-114">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="1b038-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1b038-115">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="1b038-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1b038-116">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="1b038-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1b038-117">Példák</span><span class="sxs-lookup"><span data-stu-id="1b038-117">EXAMPLES</span></span>

### <span data-ttu-id="1b038-118">1. példa: az integrációs fiók tanúsítványának létrehozása</span><span class="sxs-lookup"><span data-stu-id="1b038-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
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

<span data-ttu-id="1b038-119">Ez a parancs létrehozza az integrációs fiók tanúsítványát a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="1b038-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="1b038-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b038-120">PARAMETERS</span></span>

### <span data-ttu-id="1b038-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1b038-121">-CertificateName</span></span>
<span data-ttu-id="1b038-122">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-122">Specifies a name for the integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b038-123">-DefaultProfile</span></span>
<span data-ttu-id="1b038-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1b038-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b038-125">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="1b038-125">-KeyName</span></span>
<span data-ttu-id="1b038-126">A kulcsfájl nevét adja meg a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="1b038-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1b038-127">-KeyVaultId</span></span>
<span data-ttu-id="1b038-128">Egy kulcs-Vault-azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1b038-129">-KeyVersion</span></span>
<span data-ttu-id="1b038-130">A kulcsfájl verziószámát adja meg a Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="1b038-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1b038-131">-Metadata</span></span>
<span data-ttu-id="1b038-132">A tanúsítvány metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="1b038-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1b038-133">-Name</span></span>
<span data-ttu-id="1b038-134">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-134">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1b038-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="1b038-136">A nyilvános tanúsítvány (. cer) fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b038-137">-ResourceGroupName</span></span>
<span data-ttu-id="1b038-138">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b038-138">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b038-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b038-139">-Confirm</span></span>
<span data-ttu-id="1b038-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b038-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b038-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b038-141">-WhatIf</span></span>
<span data-ttu-id="1b038-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b038-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b038-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b038-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b038-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b038-144">CommonParameters</span></span>
<span data-ttu-id="1b038-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b038-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b038-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b038-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b038-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b038-147">INPUTS</span></span>

### <span data-ttu-id="1b038-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1b038-148">System.String</span></span>

## <span data-ttu-id="1b038-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b038-149">OUTPUTS</span></span>

### <span data-ttu-id="1b038-150">Microsoft. Azure. Management. Logic. models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1b038-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="1b038-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b038-151">NOTES</span></span>

## <span data-ttu-id="1b038-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b038-152">RELATED LINKS</span></span>

[<span data-ttu-id="1b038-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1b038-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1b038-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1b038-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1b038-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1b038-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


