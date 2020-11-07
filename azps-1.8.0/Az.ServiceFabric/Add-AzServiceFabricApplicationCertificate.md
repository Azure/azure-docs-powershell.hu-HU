---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669126"
---
# <span data-ttu-id="62c3e-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="62c3e-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="62c3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="62c3e-103">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="62c3e-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="62c3e-104">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="62c3e-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="62c3e-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62c3e-105">SYNTAX</span></span>

### <span data-ttu-id="62c3e-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="62c3e-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c3e-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="62c3e-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c3e-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="62c3e-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62c3e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="62c3e-109">DESCRIPTION</span></span>
<span data-ttu-id="62c3e-110">A **Add-AzServiceFabricApplicationCertificate** használatával telepítsen tanúsítványt a fürt összes csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="62c3e-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="62c3e-111">Megadhatja a már meglévő tanúsítványokat, vagy megadhatja, hogy a rendszer létrehoz egy újat, és feltölti egy új vagy meglévő Azure-fő boltozatra.</span><span class="sxs-lookup"><span data-stu-id="62c3e-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="62c3e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="62c3e-112">EXAMPLES</span></span>

### <span data-ttu-id="62c3e-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62c3e-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="62c3e-114">Ez a parancs a meglévő Azure Key Vault tanúsítványát fogja hozzáadni a fürt minden csomópont-típusához.</span><span class="sxs-lookup"><span data-stu-id="62c3e-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="62c3e-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="62c3e-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="62c3e-116">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, amelyen a fő pince-erőforráscsoport neve és a kulcsfájl neve látható, a fürt összes csomópont-típusára települ, és a "c:\test" mappa alatt letölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="62c3e-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="62c3e-117">A letöltendő tanúsítvány neve megegyezik a kulcsfájl-tanúsítvány nevével.</span><span class="sxs-lookup"><span data-stu-id="62c3e-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="62c3e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62c3e-118">PARAMETERS</span></span>

### <span data-ttu-id="62c3e-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="62c3e-119">-CertificateCommonName</span></span>
<span data-ttu-id="62c3e-120">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="62c3e-120">Certificate common name</span></span>

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

### <span data-ttu-id="62c3e-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="62c3e-121">-CertificateFile</span></span>
<span data-ttu-id="62c3e-122">A meglévő tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="62c3e-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="62c3e-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="62c3e-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="62c3e-124">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="62c3e-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="62c3e-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="62c3e-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="62c3e-126">A létrehozandó új tanúsítvány mappa elérési útja.</span><span class="sxs-lookup"><span data-stu-id="62c3e-126">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="62c3e-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="62c3e-127">-CertificatePassword</span></span>
<span data-ttu-id="62c3e-128">A pfx-fájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="62c3e-128">The password of the pfx file.</span></span>

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

### <span data-ttu-id="62c3e-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="62c3e-129">-CertificateSubjectName</span></span>
<span data-ttu-id="62c3e-130">A létrehozandó tanúsítvány DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="62c3e-130">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="62c3e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c3e-131">-DefaultProfile</span></span>
<span data-ttu-id="62c3e-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62c3e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c3e-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="62c3e-133">-KeyVaultName</span></span>
<span data-ttu-id="62c3e-134">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="62c3e-134">Azure key vault name.</span></span>

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

### <span data-ttu-id="62c3e-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c3e-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="62c3e-136">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="62c3e-136">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="62c3e-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62c3e-137">-Name</span></span>
<span data-ttu-id="62c3e-138">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="62c3e-138">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="62c3e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c3e-139">-ResourceGroupName</span></span>
<span data-ttu-id="62c3e-140">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="62c3e-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="62c3e-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="62c3e-141">-SecretIdentifier</span></span>
<span data-ttu-id="62c3e-142">A meglévő Azure Key Vault titkos URI-azonosító.</span><span class="sxs-lookup"><span data-stu-id="62c3e-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="62c3e-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62c3e-143">-Confirm</span></span>
<span data-ttu-id="62c3e-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62c3e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c3e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c3e-145">-WhatIf</span></span>
<span data-ttu-id="62c3e-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62c3e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62c3e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62c3e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c3e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c3e-148">CommonParameters</span></span>
<span data-ttu-id="62c3e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62c3e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c3e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c3e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c3e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c3e-151">INPUTS</span></span>

### <span data-ttu-id="62c3e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="62c3e-152">System.String</span></span>

### <span data-ttu-id="62c3e-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="62c3e-153">System.Security.SecureString</span></span>

## <span data-ttu-id="62c3e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c3e-154">OUTPUTS</span></span>

### <span data-ttu-id="62c3e-155">Microsoft. Azure. Command. ServiceFabric. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="62c3e-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="62c3e-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62c3e-156">NOTES</span></span>

## <span data-ttu-id="62c3e-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c3e-157">RELATED LINKS</span></span>

[<span data-ttu-id="62c3e-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="62c3e-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="62c3e-159">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="62c3e-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
