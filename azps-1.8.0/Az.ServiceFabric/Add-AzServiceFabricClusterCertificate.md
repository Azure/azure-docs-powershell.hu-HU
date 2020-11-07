---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669125"
---
# <span data-ttu-id="94683-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="94683-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="94683-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94683-102">SYNOPSIS</span></span>
<span data-ttu-id="94683-103">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="94683-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="94683-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94683-104">SYNTAX</span></span>

### <span data-ttu-id="94683-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="94683-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94683-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="94683-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94683-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="94683-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94683-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="94683-108">DESCRIPTION</span></span>
<span data-ttu-id="94683-109">A **Add-AzServiceFabricClusterCertificate** segítségével másodlagos fürtcsomópont vehető fel, akár egy meglévő Azure-kulccsal, akár egy új, az új, saját maga által aláírt tanúsítványon keresztül.</span><span class="sxs-lookup"><span data-stu-id="94683-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="94683-110">Ha van, akkor a másodlagos fürtöt felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="94683-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="94683-111">Példák</span><span class="sxs-lookup"><span data-stu-id="94683-111">EXAMPLES</span></span>

### <span data-ttu-id="94683-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94683-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="94683-113">Ez a parancs másodlagos fürtcsomópontként hozzáadja a meglévő Azure Key Vault tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="94683-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="94683-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="94683-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="94683-115">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, és frissíti a fürtöt, hogy másodlagos fürtcsomóponton használja azt.</span><span class="sxs-lookup"><span data-stu-id="94683-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="94683-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94683-116">PARAMETERS</span></span>

### <span data-ttu-id="94683-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="94683-117">-CertificateCommonName</span></span>
<span data-ttu-id="94683-118">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="94683-118">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94683-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="94683-119">-CertificateFile</span></span>
<span data-ttu-id="94683-120">A meglévő tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="94683-120">The existing certificate file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="94683-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="94683-122">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="94683-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94683-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="94683-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="94683-124">A létrehozandó új tanúsítvány mappája.</span><span class="sxs-lookup"><span data-stu-id="94683-124">The folder of the new certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="94683-125">-CertificatePassword</span></span>
<span data-ttu-id="94683-126">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="94683-126">The password of the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="94683-127">-CertificateSubjectName</span></span>
<span data-ttu-id="94683-128">A létrehozandó tanúsítvány DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="94683-128">The Dns name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94683-129">-DefaultProfile</span></span>
<span data-ttu-id="94683-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94683-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94683-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="94683-131">-KeyVaultName</span></span>
<span data-ttu-id="94683-132">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="94683-132">Azure key vault name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="94683-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="94683-134">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="94683-134">Azure key vault resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94683-135">-Name</span></span>
<span data-ttu-id="94683-136">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="94683-136">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94683-137">-ResourceGroupName</span></span>
<span data-ttu-id="94683-138">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94683-138">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="94683-139">-SecretIdentifier</span></span>
<span data-ttu-id="94683-140">A meglévő Azure Key Vault titkos URL-címe.</span><span class="sxs-lookup"><span data-stu-id="94683-140">The existing Azure key vault secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94683-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94683-141">-Confirm</span></span>
<span data-ttu-id="94683-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94683-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94683-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94683-143">-WhatIf</span></span>
<span data-ttu-id="94683-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94683-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94683-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94683-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94683-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94683-146">CommonParameters</span></span>
<span data-ttu-id="94683-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94683-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94683-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94683-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94683-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94683-149">INPUTS</span></span>

### <span data-ttu-id="94683-150">System. String</span><span class="sxs-lookup"><span data-stu-id="94683-150">System.String</span></span>

### <span data-ttu-id="94683-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="94683-151">System.Security.SecureString</span></span>

## <span data-ttu-id="94683-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94683-152">OUTPUTS</span></span>

### <span data-ttu-id="94683-153">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="94683-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="94683-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94683-154">NOTES</span></span>

## <span data-ttu-id="94683-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94683-155">RELATED LINKS</span></span>

[<span data-ttu-id="94683-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="94683-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="94683-157">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="94683-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="94683-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="94683-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
