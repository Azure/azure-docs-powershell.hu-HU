---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 00acd3e13484fe2981d172b4331ff7848c78fc9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502068"
---
# <span data-ttu-id="593e0-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="593e0-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="593e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="593e0-102">SYNOPSIS</span></span>
<span data-ttu-id="593e0-103">Módosítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="593e0-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="593e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="593e0-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="593e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="593e0-105">DESCRIPTION</span></span>
<span data-ttu-id="593e0-106">A **set-AzureRmIntegrationAccountCertificate** parancsmag módosította az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="593e0-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="593e0-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók tanúsítványát képviseli.</span><span class="sxs-lookup"><span data-stu-id="593e0-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="593e0-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="593e0-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="593e0-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="593e0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="593e0-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="593e0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="593e0-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="593e0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="593e0-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="593e0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="593e0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="593e0-113">EXAMPLES</span></span>

### <span data-ttu-id="593e0-114">Példa 1: az integrációs fiók tanúsítványának módosítása</span><span class="sxs-lookup"><span data-stu-id="593e0-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="593e0-115">Ez a parancs módosítja az integrációs fiók tanúsítványát a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="593e0-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="593e0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="593e0-116">PARAMETERS</span></span>

### <span data-ttu-id="593e0-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="593e0-117">-CertificateName</span></span>
<span data-ttu-id="593e0-118">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="593e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593e0-119">-DefaultProfile</span></span>
<span data-ttu-id="593e0-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="593e0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="593e0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="593e0-121">-Force</span></span>
<span data-ttu-id="593e0-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="593e0-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="593e0-123">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="593e0-123">-KeyName</span></span>
<span data-ttu-id="593e0-124">A kulcsfájl nevét adja meg a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="593e0-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="593e0-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="593e0-125">-KeyVaultId</span></span>
<span data-ttu-id="593e0-126">Egy kulcs-Vault-azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="593e0-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="593e0-127">-KeyVersion</span></span>
<span data-ttu-id="593e0-128">A kulcsfájl verziószámát adja meg a Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="593e0-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="593e0-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="593e0-129">-Metadata</span></span>
<span data-ttu-id="593e0-130">A tanúsítvány metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="593e0-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="593e0-131">-Name</span></span>
<span data-ttu-id="593e0-132">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="593e0-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="593e0-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="593e0-134">A nyilvános tanúsítvány (. cer) fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="593e0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593e0-135">-ResourceGroupName</span></span>
<span data-ttu-id="593e0-136">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="593e0-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="593e0-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="593e0-137">-Confirm</span></span>
<span data-ttu-id="593e0-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="593e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="593e0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="593e0-139">-WhatIf</span></span>
<span data-ttu-id="593e0-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="593e0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="593e0-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="593e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="593e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593e0-142">CommonParameters</span></span>
<span data-ttu-id="593e0-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="593e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593e0-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="593e0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593e0-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="593e0-145">INPUTS</span></span>

### <span data-ttu-id="593e0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="593e0-146">System.String</span></span>

## <span data-ttu-id="593e0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="593e0-147">OUTPUTS</span></span>

### <span data-ttu-id="593e0-148">Microsoft. Azure. Management. Logic. models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="593e0-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="593e0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="593e0-149">NOTES</span></span>

## <span data-ttu-id="593e0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="593e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="593e0-151">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="593e0-151">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="593e0-152">Új – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="593e0-152">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="593e0-153">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="593e0-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

