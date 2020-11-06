---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: fb52675187cda4ffd87b7198a4ffb98c2f4e4734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501388"
---
# <span data-ttu-id="02e05-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="02e05-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="02e05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02e05-102">SYNOPSIS</span></span>
<span data-ttu-id="02e05-103">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="02e05-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="02e05-104">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="02e05-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e05-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02e05-105">SYNTAX</span></span>

### <span data-ttu-id="02e05-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="02e05-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02e05-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="02e05-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02e05-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="02e05-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02e05-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="02e05-109">DESCRIPTION</span></span>
<span data-ttu-id="02e05-110">A **Add-AzureRmServiceFabricApplicationCertificate** használatával telepítsen tanúsítványt a fürt összes csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="02e05-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="02e05-111">Megadhatja a már meglévő tanúsítványokat, vagy megadhatja, hogy a rendszer létrehoz egy újat, és feltölti egy új vagy meglévő Azure-fő boltozatra.</span><span class="sxs-lookup"><span data-stu-id="02e05-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="02e05-112">Példák</span><span class="sxs-lookup"><span data-stu-id="02e05-112">EXAMPLES</span></span>

### <span data-ttu-id="02e05-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="02e05-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="02e05-114">Ez a parancs a meglévő Azure Key Vault tanúsítványát fogja hozzáadni a fürt minden csomópont-típusához.</span><span class="sxs-lookup"><span data-stu-id="02e05-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="02e05-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="02e05-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="02e05-116">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, amelyen a fő pince-erőforráscsoport neve és a kulcsfájl neve látható, a fürt összes csomópont-típusára települ, és a "c:\test" mappa alatt letölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="02e05-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="02e05-117">A letöltendő tanúsítvány neve megegyezik a kulcsfájl-tanúsítvány nevével.</span><span class="sxs-lookup"><span data-stu-id="02e05-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="02e05-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02e05-118">PARAMETERS</span></span>

### <span data-ttu-id="02e05-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="02e05-119">-CertificateFile</span></span>
<span data-ttu-id="02e05-120">A meglévő tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="02e05-120">The existing certificate file path.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="02e05-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="02e05-122">A létrehozandó új tanúsítvány mappa elérési útja.</span><span class="sxs-lookup"><span data-stu-id="02e05-122">The folder path of the new certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="02e05-123">-CertificatePassword</span></span>
<span data-ttu-id="02e05-124">A pfx-fájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="02e05-124">The password of the pfx file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="02e05-125">-CertificateSubjectName</span></span>
<span data-ttu-id="02e05-126">A létrehozandó tanúsítvány DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="02e05-126">The Dns name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e05-127">-DefaultProfile</span></span>
<span data-ttu-id="02e05-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02e05-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-129">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="02e05-129">-KeyVaultName</span></span>
<span data-ttu-id="02e05-130">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="02e05-130">Azure key vault name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e05-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="02e05-132">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="02e05-132">Azure key vault resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02e05-133">-Name</span></span>
<span data-ttu-id="02e05-134">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="02e05-134">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e05-135">-ResourceGroupName</span></span>
<span data-ttu-id="02e05-136">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="02e05-136">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="02e05-137">-SecretIdentifier</span></span>
<span data-ttu-id="02e05-138">A meglévő Azure Key Vault titkos URI-azonosító.</span><span class="sxs-lookup"><span data-stu-id="02e05-138">The existing Azure key vault secret uri.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02e05-139">-Confirm</span></span>
<span data-ttu-id="02e05-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02e05-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e05-141">-WhatIf</span></span>
<span data-ttu-id="02e05-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02e05-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02e05-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02e05-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e05-144">CommonParameters</span></span>
<span data-ttu-id="02e05-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02e05-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e05-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e05-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e05-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e05-147">INPUTS</span></span>

### <span data-ttu-id="02e05-148">System. String</span><span class="sxs-lookup"><span data-stu-id="02e05-148">System.String</span></span>

## <span data-ttu-id="02e05-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e05-149">OUTPUTS</span></span>

### <span data-ttu-id="02e05-150">Microsoft. Azure. Command. ServiceFabric. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="02e05-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="02e05-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02e05-151">NOTES</span></span>

## <span data-ttu-id="02e05-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02e05-152">RELATED LINKS</span></span>

[<span data-ttu-id="02e05-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="02e05-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="02e05-154">Új – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="02e05-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
