---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 5c28bf3e3bb6269ff9adc3b879d58d01e15e493f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011724"
---
# <span data-ttu-id="c0239-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c0239-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c0239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0239-102">SYNOPSIS</span></span>

<span data-ttu-id="c0239-103">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="c0239-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c0239-104">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="c0239-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c0239-105">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="c0239-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="c0239-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0239-106">SYNTAX</span></span>

### <span data-ttu-id="c0239-107">ByDefaultArmTemplate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0239-107">ByDefaultArmTemplate (Default)</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0239-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c0239-108">ByExistingKeyVault</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0239-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c0239-109">ByNewPfxAndVaultName</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0239-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c0239-110">ByExistingPfxAndVaultName</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0239-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0239-111">DESCRIPTION</span></span>

<span data-ttu-id="c0239-112">A **New-AzServiceFabricCluster** parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványok segítségével új szolgáltatási szövet típusú fürtöt állíthat be.</span><span class="sxs-lookup"><span data-stu-id="c0239-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c0239-113">A használt sablon lehet egy alapértelmezett sablon vagy egy Ön által megadott egyéni sablon.</span><span class="sxs-lookup"><span data-stu-id="c0239-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="c0239-114">Megadhatja, hogy milyen mappa legyen az önaláírt tanúsítványok exportálásához vagy később a kulcs boltozatból való lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="c0239-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="c0239-115">Ha egyéni sablont és paramétert tartalmazó fájlt ad meg, nem kell megadnia a tanúsítvány adatait a paraméter-fájlban, a rendszer ezeket a paramétereket fogja kitölteni.</span><span class="sxs-lookup"><span data-stu-id="c0239-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="c0239-116">A négy lehetőség alább részletezve van.</span><span class="sxs-lookup"><span data-stu-id="c0239-116">The four options are detailed below.</span></span> <span data-ttu-id="c0239-117">Görgessen le az egyes paraméterek magyarázatához.</span><span class="sxs-lookup"><span data-stu-id="c0239-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="c0239-118">Példák</span><span class="sxs-lookup"><span data-stu-id="c0239-118">EXAMPLES</span></span>

### <span data-ttu-id="c0239-119">1. példa: csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszert adja meg a fürt telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="c0239-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="c0239-120">Ez a parancs csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszert adja meg a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="c0239-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="c0239-121">2. példa: adjon meg egy meglévő erőforrást a kulcs-tárolóban, és egy egyéni sablon segítségével telepítsen egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="c0239-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="c0239-122">Ez a parancs egy meglévő tanúsítvány-erőforrást ad meg egy kulcs-tárolóban, valamint egy egyéni sablont a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="c0239-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="c0239-123">3. példa: új fürt létrehozása egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="c0239-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="c0239-124">Adjon meg egy másik erőforráscsoport-nevet a kulcsfájl számára, és a rendszer feltölt egy új tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c0239-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="c0239-125">Ez a parancs egy új fürtöt hoz létre egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="c0239-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="c0239-126">Adjon meg egy másik erőforráscsoport-nevet a kulcsfájl számára, és a rendszer feltölt egy új tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c0239-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="c0239-127">Példa 4: saját tanúsítvány és egyéni sablon létrehozása és új fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0239-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="c0239-128">Ezzel a paranccsal hozhatja létre saját tanúsítványát és egyéni sablonját, és létrehozhat egy új fürtöt.</span><span class="sxs-lookup"><span data-stu-id="c0239-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="c0239-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0239-129">PARAMETERS</span></span>

### <span data-ttu-id="c0239-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c0239-130">-CertificateCommonName</span></span>

<span data-ttu-id="c0239-131">Tanúsítvány köznapi neve</span><span class="sxs-lookup"><span data-stu-id="c0239-131">Certificate common name</span></span>

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

### <span data-ttu-id="c0239-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0239-132">-CertificateFile</span></span>

<span data-ttu-id="c0239-133">Az elsődleges fürthálózat tanúsítványának meglévő elérési útja</span><span class="sxs-lookup"><span data-stu-id="c0239-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="c0239-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="c0239-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="c0239-135">Tanúsítvány-kibocsátási ujjlenyomat, vesszővel elválasztva, ha több</span><span class="sxs-lookup"><span data-stu-id="c0239-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="c0239-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c0239-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="c0239-137">A létrehozandó új tanúsítványfájl mappája</span><span class="sxs-lookup"><span data-stu-id="c0239-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0239-138">-CertificatePassword</span></span>

<span data-ttu-id="c0239-139">A tanúsítványfájl jelszava</span><span class="sxs-lookup"><span data-stu-id="c0239-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c0239-140">-CertificateSubjectName</span></span>

<span data-ttu-id="c0239-141">A létrehozandó tanúsítvány tulajdonosának neve</span><span class="sxs-lookup"><span data-stu-id="c0239-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c0239-142">-ClusterSize</span></span>

<span data-ttu-id="c0239-143">A fürt csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="c0239-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="c0239-144">Az alapértelmezett érték 5 csomópont</span><span class="sxs-lookup"><span data-stu-id="c0239-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0239-145">-DefaultProfile</span></span>

<span data-ttu-id="c0239-146">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0239-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0239-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c0239-147">-KeyVaultName</span></span>

<span data-ttu-id="c0239-148">Azure-kulcs boltozata – ha nem adja meg, a program alapértelmezés szerint az erőforráscsoport nevéhez rendeli a nevet.</span><span class="sxs-lookup"><span data-stu-id="c0239-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0239-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="c0239-150">Az Azure Key Vault erőforráscsoport neve (ha meg van adva) alapértelmezés szerint az erőforrás csoport neve lesz</span><span class="sxs-lookup"><span data-stu-id="c0239-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-151">-Hely</span><span class="sxs-lookup"><span data-stu-id="c0239-151">-Location</span></span>

<span data-ttu-id="c0239-152">Az erőforráscsoport helye</span><span class="sxs-lookup"><span data-stu-id="c0239-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-153">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0239-153">-Name</span></span>

<span data-ttu-id="c0239-154">Adja meg a fürt nevét, ha nem adja meg, hogy az erőforráscsoport neve megegyezik-e a csoport nevével.</span><span class="sxs-lookup"><span data-stu-id="c0239-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-155">-OS</span><span class="sxs-lookup"><span data-stu-id="c0239-155">-OS</span></span>

<span data-ttu-id="c0239-156">A fürtöt alkotó VMs operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="c0239-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0239-157">-ParameterFile</span></span>

<span data-ttu-id="c0239-158">A sablon paraméter fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c0239-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0239-159">-ResourceGroupName</span></span>

<span data-ttu-id="c0239-160">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c0239-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c0239-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0239-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="c0239-162">A másodlagos fürtcsomópont meglévő tanúsítványfájl-elérési útja</span><span class="sxs-lookup"><span data-stu-id="c0239-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0239-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="c0239-164">A tanúsítványfájl jelszava</span><span class="sxs-lookup"><span data-stu-id="c0239-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c0239-165">-SecretIdentifier</span></span>

<span data-ttu-id="c0239-166">A meglévő Azure Key Vault titkos URL-címe, például ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="c0239-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="c0239-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c0239-167">-TemplateFile</span></span>

<span data-ttu-id="c0239-168">A sablonfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c0239-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-169">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="c0239-169">-VmPassword</span></span>

<span data-ttu-id="c0239-170">A VM jelszava.</span><span class="sxs-lookup"><span data-stu-id="c0239-170">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-171">-VmSku</span><span class="sxs-lookup"><span data-stu-id="c0239-171">-VmSku</span></span>

<span data-ttu-id="c0239-172">A VM SKU</span><span class="sxs-lookup"><span data-stu-id="c0239-172">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-173">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="c0239-173">-VmUserName</span></span>

<span data-ttu-id="c0239-174">A VM-be való bejelentkezéshez használt Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c0239-174">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0239-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0239-175">-Confirm</span></span>

<span data-ttu-id="c0239-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0239-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0239-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0239-177">-WhatIf</span></span>

<span data-ttu-id="c0239-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0239-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0239-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0239-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0239-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0239-180">CommonParameters</span></span>

<span data-ttu-id="c0239-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0239-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0239-182">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0239-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0239-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0239-183">INPUTS</span></span>

### <span data-ttu-id="c0239-184">System. String</span><span class="sxs-lookup"><span data-stu-id="c0239-184">System.String</span></span>

### <span data-ttu-id="c0239-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c0239-185">System.Security.SecureString</span></span>

### <span data-ttu-id="c0239-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0239-186">System.Int32</span></span>

### <span data-ttu-id="c0239-187">Microsoft. Azure. Command. ServiceFabric. models. OperatingSystem tulajdonság</span><span class="sxs-lookup"><span data-stu-id="c0239-187">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="c0239-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0239-188">OUTPUTS</span></span>

### <span data-ttu-id="c0239-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="c0239-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="c0239-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0239-190">NOTES</span></span>

## <span data-ttu-id="c0239-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0239-191">RELATED LINKS</span></span>
