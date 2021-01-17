---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368436"
---
# <span data-ttu-id="e46e5-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e46e5-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e46e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e46e5-103">Módosítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="e46e5-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="e46e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e46e5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e46e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e46e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e46e5-106">A **Set-AzIntegrationAccountCertificate** parancsmag módosítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="e46e5-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="e46e5-107">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiók tanúsítványát képviseli.</span><span class="sxs-lookup"><span data-stu-id="e46e5-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="e46e5-108">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="e46e5-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="e46e5-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="e46e5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e46e5-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="e46e5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e46e5-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="e46e5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e46e5-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="e46e5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e46e5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e46e5-113">EXAMPLES</span></span>

### <span data-ttu-id="e46e5-114">1. példa: Integrációs fiók tanúsítványának módosítása</span><span class="sxs-lookup"><span data-stu-id="e46e5-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="e46e5-115">Ez a parancs módosítja az integrációs fiók tanúsítványát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e46e5-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="e46e5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e46e5-116">PARAMETERS</span></span>

### <span data-ttu-id="e46e5-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e46e5-117">-CertificateName</span></span>
<span data-ttu-id="e46e5-118">Egy integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-118">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e46e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46e5-119">-DefaultProfile</span></span>
<span data-ttu-id="e46e5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e46e5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e46e5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e46e5-121">-Force</span></span>
<span data-ttu-id="e46e5-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e46e5-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e5-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e46e5-123">-KeyName</span></span>
<span data-ttu-id="e46e5-124">A kulcstárolóban tárolt tanúsítványkulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e46e5-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e46e5-125">-KeyVaultId</span></span>
<span data-ttu-id="e46e5-126">Egy kulcs tárolóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="e46e5-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e46e5-127">-KeyVersion</span></span>
<span data-ttu-id="e46e5-128">A kulcstárolóban a tanúsítványkulcs verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e46e5-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e46e5-129">-Metadata</span></span>
<span data-ttu-id="e46e5-130">A tanúsítvány metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="e46e5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e46e5-131">-Name</span></span>
<span data-ttu-id="e46e5-132">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e46e5-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e46e5-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="e46e5-134">Egy nyilvános tanúsítványfájl (.cer) elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="e46e5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46e5-135">-ResourceGroupName</span></span>
<span data-ttu-id="e46e5-136">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46e5-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e46e5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e46e5-137">-Confirm</span></span>
<span data-ttu-id="e46e5-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e46e5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46e5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46e5-139">-WhatIf</span></span>
<span data-ttu-id="e46e5-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e46e5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46e5-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e46e5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46e5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46e5-142">CommonParameters</span></span>
<span data-ttu-id="e46e5-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e46e5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46e5-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e46e5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46e5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e46e5-145">INPUTS</span></span>

### <span data-ttu-id="e46e5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e46e5-146">System.String</span></span>

## <span data-ttu-id="e46e5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e46e5-147">OUTPUTS</span></span>

### <span data-ttu-id="e46e5-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e46e5-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e46e5-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e46e5-149">NOTES</span></span>

## <span data-ttu-id="e46e5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e46e5-150">RELATED LINKS</span></span>

[<span data-ttu-id="e46e5-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e46e5-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e46e5-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e46e5-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e46e5-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e46e5-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


