---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 8a35bb9be2da954c6ca0c51f97af9bffb3e373c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493018"
---
# <span data-ttu-id="ddb71-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb71-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="ddb71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddb71-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb71-103">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ddb71-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddb71-104">SYNTAX</span></span>

### <span data-ttu-id="ddb71-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="ddb71-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddb71-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ddb71-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb71-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ddb71-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddb71-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddb71-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb71-109">A **Add-AzureRmServiceFabricClusterCertificate** segítségével másodlagos fürtcsomópont vehető fel, akár egy meglévő Azure-kulccsal, akár egy új, az új, saját maga által aláírt tanúsítványon keresztül.</span><span class="sxs-lookup"><span data-stu-id="ddb71-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="ddb71-110">Ha van, akkor a másodlagos fürtöt felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="ddb71-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="ddb71-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ddb71-111">EXAMPLES</span></span>

### <span data-ttu-id="ddb71-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ddb71-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="ddb71-113">Ez a parancs másodlagos fürtcsomópontként hozzáadja a meglévő Azure Key Vault tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="ddb71-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="ddb71-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ddb71-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="ddb71-115">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, és frissíti a fürtöt, hogy másodlagos fürtcsomóponton használja azt.</span><span class="sxs-lookup"><span data-stu-id="ddb71-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="ddb71-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddb71-116">PARAMETERS</span></span>

### <span data-ttu-id="ddb71-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ddb71-117">-CertificateFile</span></span>
<span data-ttu-id="ddb71-118">A meglévő tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ddb71-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="ddb71-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="ddb71-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="ddb71-120">A létrehozandó új tanúsítvány mappája.</span><span class="sxs-lookup"><span data-stu-id="ddb71-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="ddb71-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ddb71-121">-CertificatePassword</span></span>
<span data-ttu-id="ddb71-122">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="ddb71-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="ddb71-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="ddb71-123">-CertificateSubjectName</span></span>
<span data-ttu-id="ddb71-124">A létrehozandó tanúsítvány DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="ddb71-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="ddb71-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb71-125">-DefaultProfile</span></span>
<span data-ttu-id="ddb71-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddb71-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb71-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="ddb71-127">-KeyVaultName</span></span>
<span data-ttu-id="ddb71-128">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="ddb71-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="ddb71-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb71-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="ddb71-130">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ddb71-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="ddb71-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddb71-131">-Name</span></span>
<span data-ttu-id="ddb71-132">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ddb71-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ddb71-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb71-133">-ResourceGroupName</span></span>
<span data-ttu-id="ddb71-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddb71-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ddb71-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="ddb71-135">-SecretIdentifier</span></span>
<span data-ttu-id="ddb71-136">A meglévő Azure Key Vault titkos URL-címe.</span><span class="sxs-lookup"><span data-stu-id="ddb71-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="ddb71-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddb71-137">-Confirm</span></span>
<span data-ttu-id="ddb71-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddb71-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb71-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb71-139">-WhatIf</span></span>
<span data-ttu-id="ddb71-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddb71-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddb71-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddb71-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb71-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb71-142">CommonParameters</span></span>
<span data-ttu-id="ddb71-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddb71-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb71-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb71-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb71-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb71-145">INPUTS</span></span>

### <span data-ttu-id="ddb71-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb71-146">System.String</span></span>

## <span data-ttu-id="ddb71-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb71-147">OUTPUTS</span></span>

### <span data-ttu-id="ddb71-148">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="ddb71-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ddb71-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddb71-149">NOTES</span></span>

## <span data-ttu-id="ddb71-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddb71-150">RELATED LINKS</span></span>

[<span data-ttu-id="ddb71-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb71-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="ddb71-152">Új – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ddb71-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="ddb71-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb71-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
