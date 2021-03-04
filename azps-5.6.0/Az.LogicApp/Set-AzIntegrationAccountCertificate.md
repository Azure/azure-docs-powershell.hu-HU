---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: c7ae1404cfff2d725326b9f5a8f2b7244c030109
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941817"
---
# <span data-ttu-id="0a5be-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0a5be-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="0a5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5be-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5be-103">Módosítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="0a5be-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="0a5be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a5be-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a5be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a5be-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5be-106">A **Set-AzIntegrationAccountCertificate** parancsmag módosítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="0a5be-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="0a5be-107">Ez a parancsmag egy olyan objektumot ad vissza, amely az integrációs fiók tanúsítványát képviseli.</span><span class="sxs-lookup"><span data-stu-id="0a5be-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="0a5be-108">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="0a5be-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="0a5be-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0a5be-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0a5be-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0a5be-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0a5be-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="0a5be-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a5be-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="0a5be-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a5be-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a5be-113">EXAMPLES</span></span>

### <span data-ttu-id="0a5be-114">1. példa: Integrációs fiók tanúsítványának módosítása</span><span class="sxs-lookup"><span data-stu-id="0a5be-114">Example 1: Modify an integration account certificate</span></span>
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

<span data-ttu-id="0a5be-115">Ez a parancs módosítja az integrációs fiók tanúsítványát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="0a5be-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="0a5be-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5be-116">PARAMETERS</span></span>

### <span data-ttu-id="0a5be-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0a5be-117">-CertificateName</span></span>
<span data-ttu-id="0a5be-118">Egy integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="0a5be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5be-119">-DefaultProfile</span></span>
<span data-ttu-id="0a5be-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a5be-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a5be-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0a5be-121">-Force</span></span>
<span data-ttu-id="0a5be-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0a5be-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a5be-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0a5be-123">-KeyName</span></span>
<span data-ttu-id="0a5be-124">A kulcstárolóban tárolt tanúsítványkulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="0a5be-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0a5be-125">-KeyVaultId</span></span>
<span data-ttu-id="0a5be-126">Egy kulcs tárolóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="0a5be-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="0a5be-127">-KeyVersion</span></span>
<span data-ttu-id="0a5be-128">A kulcstárolóban a tanúsítványkulcs verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="0a5be-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0a5be-129">-Metadata</span></span>
<span data-ttu-id="0a5be-130">A tanúsítvány metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="0a5be-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0a5be-131">-Name</span></span>
<span data-ttu-id="0a5be-132">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0a5be-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0a5be-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="0a5be-134">Egy nyilvános tanúsítványfájl (.cer) elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="0a5be-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5be-135">-ResourceGroupName</span></span>
<span data-ttu-id="0a5be-136">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a5be-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0a5be-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5be-137">-Confirm</span></span>
<span data-ttu-id="0a5be-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a5be-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5be-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5be-139">-WhatIf</span></span>
<span data-ttu-id="0a5be-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a5be-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5be-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a5be-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5be-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5be-142">CommonParameters</span></span>
<span data-ttu-id="0a5be-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5be-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5be-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5be-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5be-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a5be-145">INPUTS</span></span>

### <span data-ttu-id="0a5be-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0a5be-146">System.String</span></span>

## <span data-ttu-id="0a5be-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a5be-147">OUTPUTS</span></span>

### <span data-ttu-id="0a5be-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0a5be-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="0a5be-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a5be-149">NOTES</span></span>

## <span data-ttu-id="0a5be-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a5be-150">RELATED LINKS</span></span>

[<span data-ttu-id="0a5be-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0a5be-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="0a5be-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0a5be-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="0a5be-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0a5be-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


