---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838782"
---
# <span data-ttu-id="0bc1f-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0bc1f-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="0bc1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bc1f-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc1f-103">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="0bc1f-104">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="0bc1f-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bc1f-105">SYNTAX</span></span>

### <span data-ttu-id="0bc1f-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="0bc1f-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc1f-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc1f-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bc1f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bc1f-109">DESCRIPTION</span></span>
<span data-ttu-id="0bc1f-110">A **Add-AzServiceFabricApplicationCertificate** használatával telepítsen tanúsítványt a fürt összes csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="0bc1f-111">Megadhatja a már meglévő tanúsítványokat, vagy megadhatja, hogy a rendszer létrehoz egy újat, és feltölti egy új vagy meglévő Azure-fő boltozatra.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="0bc1f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0bc1f-112">EXAMPLES</span></span>

### <span data-ttu-id="0bc1f-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0bc1f-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="0bc1f-114">Ez a parancs a meglévő Azure Key Vault tanúsítványát fogja hozzáadni a fürt minden csomópont-típusához.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="0bc1f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="0bc1f-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="0bc1f-116">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, amelyen a fő pince-erőforráscsoport neve és a kulcsfájl neve látható, a fürt összes csomópont-típusára települ, és a "c:\test" mappa alatt letölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="0bc1f-117">A letöltendő tanúsítvány neve megegyezik a kulcsfájl-tanúsítvány nevével.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="0bc1f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bc1f-118">PARAMETERS</span></span>

### <span data-ttu-id="0bc1f-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-119">-CertificateCommonName</span></span>
<span data-ttu-id="0bc1f-120">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="0bc1f-120">Certificate common name</span></span>

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

### <span data-ttu-id="0bc1f-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0bc1f-121">-CertificateFile</span></span>
<span data-ttu-id="0bc1f-122">A meglévő tanúsítvány elérési útja</span><span class="sxs-lookup"><span data-stu-id="0bc1f-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="0bc1f-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="0bc1f-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="0bc1f-124">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="0bc1f-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="0bc1f-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="0bc1f-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="0bc1f-126">Az a mappa, ahol az új tanúsítványt le kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="0bc1f-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0bc1f-127">-CertificatePassword</span></span>
<span data-ttu-id="0bc1f-128">A tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="0bc1f-128">The password of the certificate</span></span>

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

### <span data-ttu-id="0bc1f-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-129">-CertificateSubjectName</span></span>
<span data-ttu-id="0bc1f-130">A tanúsítvány tulajdonosának neve</span><span class="sxs-lookup"><span data-stu-id="0bc1f-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="0bc1f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc1f-131">-DefaultProfile</span></span>
<span data-ttu-id="0bc1f-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bc1f-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-133">-KeyVaultName</span></span>
<span data-ttu-id="0bc1f-134">Azure-kulcs boltozata – ha nem adja meg, a program alapértelmezés szerint az erőforráscsoport nevéhez rendeli a nevet.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="0bc1f-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="0bc1f-136">Az Azure Key Vault erőforráscsoport neve (ha meg van adva) alapértelmezés szerint az erőforrás csoport neve lesz</span><span class="sxs-lookup"><span data-stu-id="0bc1f-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="0bc1f-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0bc1f-137">-Name</span></span>
<span data-ttu-id="0bc1f-138">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="0bc1f-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0bc1f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc1f-139">-ResourceGroupName</span></span>
<span data-ttu-id="0bc1f-140">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0bc1f-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="0bc1f-141">-SecretIdentifier</span></span>
<span data-ttu-id="0bc1f-142">A meglévő Azure Key Vault titkos URL-címe, például ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="0bc1f-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="0bc1f-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0bc1f-143">-Confirm</span></span>
<span data-ttu-id="0bc1f-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc1f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc1f-145">-WhatIf</span></span>
<span data-ttu-id="0bc1f-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc1f-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bc1f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc1f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc1f-148">CommonParameters</span></span>
<span data-ttu-id="0bc1f-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bc1f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc1f-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc1f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc1f-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bc1f-151">INPUTS</span></span>

### <span data-ttu-id="0bc1f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc1f-152">System.String</span></span>

### <span data-ttu-id="0bc1f-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0bc1f-153">System.Security.SecureString</span></span>

## <span data-ttu-id="0bc1f-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bc1f-154">OUTPUTS</span></span>

### <span data-ttu-id="0bc1f-155">Microsoft. Azure. Command. ServiceFabric. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0bc1f-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="0bc1f-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bc1f-156">NOTES</span></span>

## <span data-ttu-id="0bc1f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bc1f-157">RELATED LINKS</span></span>

[<span data-ttu-id="0bc1f-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0bc1f-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="0bc1f-159">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0bc1f-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
