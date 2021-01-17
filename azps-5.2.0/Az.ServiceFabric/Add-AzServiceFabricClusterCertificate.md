---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348642"
---
# <span data-ttu-id="8271e-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8271e-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="8271e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8271e-102">SYNOPSIS</span></span>
<span data-ttu-id="8271e-103">Vegyen fel egy másodlagos fürt tanúsítványát a fürtbe.</span><span class="sxs-lookup"><span data-stu-id="8271e-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="8271e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8271e-104">SYNTAX</span></span>

### <span data-ttu-id="8271e-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="8271e-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8271e-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="8271e-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8271e-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="8271e-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8271e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8271e-108">DESCRIPTION</span></span>
<span data-ttu-id="8271e-109">Az **Add-AzServiceFabricClusterCertificate** segítségével másodlagos fürttanúsítványt adhat hozzá egy meglévő Azure-kulcstárolóból, vagy egy meglévő tanúsítvány használatával új Azure-kulcstárolót hoz létre, vagy egy új önaírt tanúsítványból.</span><span class="sxs-lookup"><span data-stu-id="8271e-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="8271e-110">Ha van ilyen, felülírja a másodlagos fürtöt.</span><span class="sxs-lookup"><span data-stu-id="8271e-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="8271e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8271e-111">EXAMPLES</span></span>

### <span data-ttu-id="8271e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8271e-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="8271e-113">Ez a parancs hozzáad egy tanúsítványt a meglévő Azure-kulcstárolóhoz másodlagos fürt tanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="8271e-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="8271e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8271e-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="8271e-115">Ez a parancs létrehoz egy öna aláírt tanúsítványt az Azure-kulcstárolóban, és frissíti a fürtöt, hogy másodlagos fürt tanúsítványként használja.</span><span class="sxs-lookup"><span data-stu-id="8271e-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="8271e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8271e-116">PARAMETERS</span></span>

### <span data-ttu-id="8271e-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="8271e-117">-CertificateCommonName</span></span>
<span data-ttu-id="8271e-118">Tanúsítvány általános neve</span><span class="sxs-lookup"><span data-stu-id="8271e-118">Certificate common name</span></span>

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

### <span data-ttu-id="8271e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8271e-119">-CertificateFile</span></span>
<span data-ttu-id="8271e-120">A meglévő tanúsítvány elérési útja</span><span class="sxs-lookup"><span data-stu-id="8271e-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="8271e-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="8271e-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="8271e-122">A tanúsítvány kibocsátójának thumbprint, separated by vessző if more than one</span><span class="sxs-lookup"><span data-stu-id="8271e-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="8271e-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="8271e-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="8271e-124">Az a mappa, amelybe le kell tölteni az új tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="8271e-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="8271e-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8271e-125">-CertificatePassword</span></span>
<span data-ttu-id="8271e-126">A tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="8271e-126">The password of the certificate</span></span>

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

### <span data-ttu-id="8271e-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="8271e-127">-CertificateSubjectName</span></span>
<span data-ttu-id="8271e-128">A tanúsítvány tárgya</span><span class="sxs-lookup"><span data-stu-id="8271e-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="8271e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8271e-129">-DefaultProfile</span></span>
<span data-ttu-id="8271e-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8271e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8271e-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="8271e-131">-KeyVaultName</span></span>
<span data-ttu-id="8271e-132">Azure-kulcstár neve, ha nincs megadva, az erőforráscsoport neve lesz alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8271e-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="8271e-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8271e-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="8271e-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span><span class="sxs-lookup"><span data-stu-id="8271e-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="8271e-135">-Name</span><span class="sxs-lookup"><span data-stu-id="8271e-135">-Name</span></span>
<span data-ttu-id="8271e-136">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="8271e-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="8271e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8271e-137">-ResourceGroupName</span></span>
<span data-ttu-id="8271e-138">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="8271e-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8271e-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="8271e-139">-SecretIdentifier</span></span>
<span data-ttu-id="8271e-140">A meglévő Azure-kulcstár titkos URL-címe, például https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="8271e-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="8271e-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="8271e-141">-Thumbprint</span></span>
<span data-ttu-id="8271e-142">A tanúsítvány thumbprint for correspoinding to the SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="8271e-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="8271e-143">Ezt akkor használja, ha a tanúsítvány kezelése nem úgy történik, hogy a kulcstároló csak titkosként tárolná a tanúsítványt, és a parancsmag nem tudja visszaírni a thumbprintet.</span><span class="sxs-lookup"><span data-stu-id="8271e-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="8271e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8271e-144">-Confirm</span></span>
<span data-ttu-id="8271e-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8271e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8271e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8271e-146">-WhatIf</span></span>
<span data-ttu-id="8271e-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8271e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8271e-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8271e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8271e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8271e-149">CommonParameters</span></span>
<span data-ttu-id="8271e-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8271e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8271e-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8271e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8271e-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8271e-152">INPUTS</span></span>

### <span data-ttu-id="8271e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="8271e-153">System.String</span></span>

### <span data-ttu-id="8271e-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="8271e-154">System.Security.SecureString</span></span>

## <span data-ttu-id="8271e-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8271e-155">OUTPUTS</span></span>

### <span data-ttu-id="8271e-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8271e-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8271e-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8271e-157">NOTES</span></span>

## <span data-ttu-id="8271e-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8271e-158">RELATED LINKS</span></span>

[<span data-ttu-id="8271e-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8271e-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="8271e-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8271e-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
