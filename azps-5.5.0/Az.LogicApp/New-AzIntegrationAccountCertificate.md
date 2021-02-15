---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203723"
---
# <span data-ttu-id="b3532-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b3532-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b3532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3532-102">SYNOPSIS</span></span>
<span data-ttu-id="b3532-103">Létrehoz egy integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="b3532-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="b3532-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3532-104">SYNTAX</span></span>

### <span data-ttu-id="b3532-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="b3532-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3532-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="b3532-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3532-107">Mindkettő</span><span class="sxs-lookup"><span data-stu-id="b3532-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3532-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3532-108">DESCRIPTION</span></span>
<span data-ttu-id="b3532-109">A **New-AzIntegrationAccountCertificate parancsmag** létrehoz egy integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="b3532-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="b3532-110">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiók tanúsítványát képviseli.</span><span class="sxs-lookup"><span data-stu-id="b3532-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="b3532-111">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét, a tanúsítvány nevét, a kulcs nevét, a kulcsverziót és a kulcstároló azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b3532-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="b3532-112">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="b3532-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b3532-113">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b3532-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b3532-114">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="b3532-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b3532-115">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="b3532-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b3532-116">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="b3532-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b3532-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3532-117">EXAMPLES</span></span>

### <span data-ttu-id="b3532-118">1. példa: Integrációs fiók tanúsítványának létrehozása</span><span class="sxs-lookup"><span data-stu-id="b3532-118">Example 1: Create an integration account certificate</span></span>
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

<span data-ttu-id="b3532-119">Ez a parancs létrehozza az integrációs fiók tanúsítványát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b3532-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="b3532-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3532-120">PARAMETERS</span></span>

### <span data-ttu-id="b3532-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b3532-121">-CertificateName</span></span>
<span data-ttu-id="b3532-122">Megadja az integrációs fiók tanúsítványának nevét.</span><span class="sxs-lookup"><span data-stu-id="b3532-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="b3532-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3532-123">-DefaultProfile</span></span>
<span data-ttu-id="b3532-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b3532-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3532-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b3532-125">-KeyName</span></span>
<span data-ttu-id="b3532-126">A kulcstárolóban a tanúsítványkulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="b3532-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b3532-127">-KeyVaultId</span></span>
<span data-ttu-id="b3532-128">Egy kulcs tárolóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="b3532-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="b3532-129">-KeyVersion</span></span>
<span data-ttu-id="b3532-130">A kulcstárolóban a tanúsítványkulcs verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="b3532-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b3532-131">-Metadata</span></span>
<span data-ttu-id="b3532-132">A tanúsítvány metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="b3532-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b3532-133">-Name</span></span>
<span data-ttu-id="b3532-134">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b3532-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="b3532-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="b3532-136">Egy nyilvános tanúsítványfájl (.cer) elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="b3532-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3532-137">-ResourceGroupName</span></span>
<span data-ttu-id="b3532-138">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3532-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3532-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3532-139">-Confirm</span></span>
<span data-ttu-id="b3532-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3532-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3532-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3532-141">-WhatIf</span></span>
<span data-ttu-id="b3532-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3532-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3532-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3532-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3532-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3532-144">CommonParameters</span></span>
<span data-ttu-id="b3532-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3532-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3532-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3532-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3532-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3532-147">INPUTS</span></span>

### <span data-ttu-id="b3532-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b3532-148">System.String</span></span>

## <span data-ttu-id="b3532-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3532-149">OUTPUTS</span></span>

### <span data-ttu-id="b3532-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b3532-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="b3532-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3532-151">NOTES</span></span>

## <span data-ttu-id="b3532-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3532-152">RELATED LINKS</span></span>

[<span data-ttu-id="b3532-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b3532-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b3532-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b3532-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b3532-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b3532-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


