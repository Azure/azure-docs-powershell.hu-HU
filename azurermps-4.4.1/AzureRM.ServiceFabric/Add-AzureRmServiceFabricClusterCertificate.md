---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503187"
---
# <span data-ttu-id="0096d-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0096d-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="0096d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0096d-102">SYNOPSIS</span></span>
<span data-ttu-id="0096d-103">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="0096d-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0096d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0096d-104">SYNTAX</span></span>

### <span data-ttu-id="0096d-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="0096d-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0096d-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0096d-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0096d-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0096d-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0096d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0096d-108">DESCRIPTION</span></span>
<span data-ttu-id="0096d-109">A **Add-AzureRmServiceFabricClusterCertificate** segítségével másodlagos fürtcsomópont vehető fel, akár egy meglévő Azure-kulccsal, akár egy új, az új, saját maga által aláírt tanúsítványon keresztül.</span><span class="sxs-lookup"><span data-stu-id="0096d-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="0096d-110">Ha van, akkor a másodlagos fürtöt felülbírálja.</span><span class="sxs-lookup"><span data-stu-id="0096d-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="0096d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0096d-111">EXAMPLES</span></span>

### <span data-ttu-id="0096d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0096d-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="0096d-113">Ez a parancs másodlagos fürtcsomópontként hozzáadja a meglévő Azure Key Vault tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="0096d-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="0096d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0096d-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="0096d-115">Ez a parancs létrehoz egy önaláírt tanúsítványt az Azure Key Vault-ban, és frissíti a fürtöt, hogy másodlagos fürtcsomóponton használja azt.</span><span class="sxs-lookup"><span data-stu-id="0096d-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="0096d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0096d-116">PARAMETERS</span></span>

### <span data-ttu-id="0096d-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0096d-117">-CertificateFile</span></span>
<span data-ttu-id="0096d-118">A meglévő tanúsítványfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0096d-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="0096d-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="0096d-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="0096d-120">A létrehozandó új tanúsítvány mappája.</span><span class="sxs-lookup"><span data-stu-id="0096d-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="0096d-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0096d-121">-CertificatePassword</span></span>
<span data-ttu-id="0096d-122">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="0096d-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="0096d-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="0096d-123">-CertificateSubjectName</span></span>
<span data-ttu-id="0096d-124">A létrehozandó tanúsítvány DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="0096d-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="0096d-125">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="0096d-125">-KeyVaultName</span></span>
<span data-ttu-id="0096d-126">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="0096d-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="0096d-127">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="0096d-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="0096d-128">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0096d-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="0096d-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0096d-129">-Name</span></span>
<span data-ttu-id="0096d-130">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="0096d-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0096d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0096d-131">-ResourceGroupName</span></span>
<span data-ttu-id="0096d-132">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0096d-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0096d-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="0096d-133">-SecretIdentifier</span></span>
<span data-ttu-id="0096d-134">A meglévő Azure Key Vault titkos URL-címe.</span><span class="sxs-lookup"><span data-stu-id="0096d-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="0096d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0096d-135">-Confirm</span></span>
<span data-ttu-id="0096d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0096d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0096d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0096d-137">-WhatIf</span></span>
<span data-ttu-id="0096d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0096d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0096d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0096d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0096d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0096d-140">-DefaultProfile</span></span>
<span data-ttu-id="0096d-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0096d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0096d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0096d-142">CommonParameters</span></span>
<span data-ttu-id="0096d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0096d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0096d-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0096d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0096d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0096d-145">INPUTS</span></span>

### <span data-ttu-id="0096d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0096d-146">System.String</span></span>

## <span data-ttu-id="0096d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0096d-147">OUTPUTS</span></span>

### <span data-ttu-id="0096d-148">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="0096d-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="0096d-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0096d-149">NOTES</span></span>

## <span data-ttu-id="0096d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0096d-150">RELATED LINKS</span></span>

[<span data-ttu-id="0096d-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0096d-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="0096d-152">Új – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0096d-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="0096d-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0096d-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
