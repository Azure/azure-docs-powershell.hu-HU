---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187992"
---
# <span data-ttu-id="eeb76-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb76-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="eeb76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eeb76-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb76-103">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="eeb76-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="eeb76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eeb76-104">SYNTAX</span></span>

### <span data-ttu-id="eeb76-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb76-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb76-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="eeb76-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb76-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="eeb76-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeb76-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eeb76-108">DESCRIPTION</span></span>
<span data-ttu-id="eeb76-109">A **Add-AzServiceFabricClusterCertificate** segítségével másodlagos fürtcsomópont vehető fel, akár egy meglévő Azure-kulccsal, akár egy új, az új, saját maga által aláírt tanúsítványon keresztül.</span><span class="sxs-lookup"><span data-stu-id="eeb76-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="eeb76-110">Ha van, akkor a másodlagos fürtöt felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="eeb76-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="eeb76-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eeb76-111">EXAMPLES</span></span>

### <span data-ttu-id="eeb76-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eeb76-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="eeb76-113">Ez a parancs másodlagos fürtcsomópontként hozzáadja a meglévő Azure Key Vault tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="eeb76-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="eeb76-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="eeb76-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="eeb76-115">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, és frissíti a fürtöt, hogy másodlagos fürtcsomóponton használja azt.</span><span class="sxs-lookup"><span data-stu-id="eeb76-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="eeb76-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eeb76-116">PARAMETERS</span></span>

### <span data-ttu-id="eeb76-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="eeb76-117">-CertificateCommonName</span></span>
<span data-ttu-id="eeb76-118">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="eeb76-118">Certificate common name</span></span>

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

### <span data-ttu-id="eeb76-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="eeb76-119">-CertificateFile</span></span>
<span data-ttu-id="eeb76-120">A meglévő tanúsítvány elérési útja</span><span class="sxs-lookup"><span data-stu-id="eeb76-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="eeb76-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="eeb76-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="eeb76-122">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="eeb76-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="eeb76-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="eeb76-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="eeb76-124">Az a mappa, ahol az új tanúsítványt le kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="eeb76-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="eeb76-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="eeb76-125">-CertificatePassword</span></span>
<span data-ttu-id="eeb76-126">A tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="eeb76-126">The password of the certificate</span></span>

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

### <span data-ttu-id="eeb76-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="eeb76-127">-CertificateSubjectName</span></span>
<span data-ttu-id="eeb76-128">A tanúsítvány tulajdonosának neve</span><span class="sxs-lookup"><span data-stu-id="eeb76-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="eeb76-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb76-129">-DefaultProfile</span></span>
<span data-ttu-id="eeb76-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eeb76-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb76-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="eeb76-131">-KeyVaultName</span></span>
<span data-ttu-id="eeb76-132">Azure-kulcs boltozata – ha nem adja meg, a program alapértelmezés szerint az erőforráscsoport nevéhez rendeli a nevet.</span><span class="sxs-lookup"><span data-stu-id="eeb76-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="eeb76-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb76-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="eeb76-134">Az Azure Key Vault erőforráscsoport neve (ha meg van adva) alapértelmezés szerint az erőforrás csoport neve lesz</span><span class="sxs-lookup"><span data-stu-id="eeb76-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="eeb76-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eeb76-135">-Name</span></span>
<span data-ttu-id="eeb76-136">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="eeb76-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="eeb76-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb76-137">-ResourceGroupName</span></span>
<span data-ttu-id="eeb76-138">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="eeb76-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eeb76-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="eeb76-139">-SecretIdentifier</span></span>
<span data-ttu-id="eeb76-140">A meglévő Azure Key Vault titkos URL-címe, például ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="eeb76-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="eeb76-141">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="eeb76-141">-Thumbprint</span></span>
<span data-ttu-id="eeb76-142">A correspoinding Tanúsítvány ujjlenyomata a SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="eeb76-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="eeb76-143">Akkor használja ezt a lehetőséget, ha a tanúsítványt nem kezeli a rendszer, mert a tanúsítvány csak titkosként van tárolva, és a parancsmag nem tudja lekérni az ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="eeb76-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb76-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eeb76-144">-Confirm</span></span>
<span data-ttu-id="eeb76-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eeb76-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb76-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb76-146">-WhatIf</span></span>
<span data-ttu-id="eeb76-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eeb76-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb76-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eeb76-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb76-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb76-149">CommonParameters</span></span>
<span data-ttu-id="eeb76-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eeb76-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb76-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eeb76-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb76-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eeb76-152">INPUTS</span></span>

### <span data-ttu-id="eeb76-153">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb76-153">System.String</span></span>

### <span data-ttu-id="eeb76-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="eeb76-154">System.Security.SecureString</span></span>

## <span data-ttu-id="eeb76-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eeb76-155">OUTPUTS</span></span>

### <span data-ttu-id="eeb76-156">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="eeb76-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="eeb76-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eeb76-157">NOTES</span></span>

## <span data-ttu-id="eeb76-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eeb76-158">RELATED LINKS</span></span>

[<span data-ttu-id="eeb76-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb76-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="eeb76-160">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="eeb76-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
