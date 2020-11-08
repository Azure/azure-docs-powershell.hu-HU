---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: dfbf9267aad981db63608c744825f1b636c85425
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011075"
---
# <span data-ttu-id="08f8e-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="08f8e-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="08f8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="08f8e-103">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="08f8e-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="08f8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08f8e-104">SYNTAX</span></span>

### <span data-ttu-id="08f8e-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="08f8e-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f8e-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="08f8e-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f8e-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="08f8e-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08f8e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="08f8e-108">DESCRIPTION</span></span>
<span data-ttu-id="08f8e-109">A **Add-AzServiceFabricClusterCertificate** segítségével másodlagos fürtcsomópont vehető fel, akár egy meglévő Azure-kulccsal, akár egy új, az új, saját maga által aláírt tanúsítványon keresztül.</span><span class="sxs-lookup"><span data-stu-id="08f8e-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="08f8e-110">Ha van, akkor a másodlagos fürtöt felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="08f8e-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="08f8e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="08f8e-111">EXAMPLES</span></span>

### <span data-ttu-id="08f8e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08f8e-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="08f8e-113">Ez a parancs másodlagos fürtcsomópontként hozzáadja a meglévő Azure Key Vault tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="08f8e-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="08f8e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="08f8e-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="08f8e-115">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, és frissíti a fürtöt, hogy másodlagos fürtcsomóponton használja azt.</span><span class="sxs-lookup"><span data-stu-id="08f8e-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="08f8e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08f8e-116">PARAMETERS</span></span>

### <span data-ttu-id="08f8e-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="08f8e-117">-CertificateCommonName</span></span>
<span data-ttu-id="08f8e-118">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="08f8e-118">Certificate common name</span></span>

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

### <span data-ttu-id="08f8e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="08f8e-119">-CertificateFile</span></span>
<span data-ttu-id="08f8e-120">A meglévő tanúsítvány elérési útja</span><span class="sxs-lookup"><span data-stu-id="08f8e-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="08f8e-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="08f8e-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="08f8e-122">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="08f8e-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="08f8e-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="08f8e-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="08f8e-124">Az a mappa, ahol az új tanúsítványt le kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="08f8e-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="08f8e-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="08f8e-125">-CertificatePassword</span></span>
<span data-ttu-id="08f8e-126">A tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="08f8e-126">The password of the certificate</span></span>

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

### <span data-ttu-id="08f8e-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="08f8e-127">-CertificateSubjectName</span></span>
<span data-ttu-id="08f8e-128">A tanúsítvány tulajdonosának neve</span><span class="sxs-lookup"><span data-stu-id="08f8e-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="08f8e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f8e-129">-DefaultProfile</span></span>
<span data-ttu-id="08f8e-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08f8e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f8e-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="08f8e-131">-KeyVaultName</span></span>
<span data-ttu-id="08f8e-132">Azure-kulcs boltozata – ha nem adja meg, a program alapértelmezés szerint az erőforráscsoport nevéhez rendeli a nevet.</span><span class="sxs-lookup"><span data-stu-id="08f8e-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="08f8e-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f8e-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="08f8e-134">Az Azure Key Vault erőforráscsoport neve (ha meg van adva) alapértelmezés szerint az erőforrás csoport neve lesz</span><span class="sxs-lookup"><span data-stu-id="08f8e-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f8e-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08f8e-135">-Name</span></span>
<span data-ttu-id="08f8e-136">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="08f8e-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="08f8e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f8e-137">-ResourceGroupName</span></span>
<span data-ttu-id="08f8e-138">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="08f8e-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="08f8e-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="08f8e-139">-SecretIdentifier</span></span>
<span data-ttu-id="08f8e-140">A meglévő Azure Key Vault titkos URL-címe, például ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="08f8e-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="08f8e-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08f8e-141">-Confirm</span></span>
<span data-ttu-id="08f8e-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08f8e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f8e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f8e-143">-WhatIf</span></span>
<span data-ttu-id="08f8e-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08f8e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f8e-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08f8e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f8e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f8e-146">CommonParameters</span></span>
<span data-ttu-id="08f8e-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08f8e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f8e-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08f8e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f8e-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08f8e-149">INPUTS</span></span>

### <span data-ttu-id="08f8e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="08f8e-150">System.String</span></span>

### <span data-ttu-id="08f8e-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="08f8e-151">System.Security.SecureString</span></span>

## <span data-ttu-id="08f8e-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08f8e-152">OUTPUTS</span></span>

### <span data-ttu-id="08f8e-153">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="08f8e-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="08f8e-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08f8e-154">NOTES</span></span>

## <span data-ttu-id="08f8e-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08f8e-155">RELATED LINKS</span></span>

[<span data-ttu-id="08f8e-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="08f8e-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="08f8e-157">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="08f8e-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
