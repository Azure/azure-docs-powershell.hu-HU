---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504727"
---
# <span data-ttu-id="03295-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="03295-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="03295-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03295-102">SYNOPSIS</span></span>
<span data-ttu-id="03295-103">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="03295-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="03295-104">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="03295-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="03295-105">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="03295-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03295-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03295-106">SYNTAX</span></span>

### <span data-ttu-id="03295-107">ByDefaultArmTemplate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03295-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03295-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="03295-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03295-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="03295-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03295-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="03295-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03295-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="03295-111">DESCRIPTION</span></span>
<span data-ttu-id="03295-112">A **New-AzureRmServiceFabricCluster** parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványok segítségével új szolgáltatási szövet típusú fürtöt állíthat be.</span><span class="sxs-lookup"><span data-stu-id="03295-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="03295-113">A használt sablon lehet egy alapértelmezett sablon vagy egy Ön által megadott egyéni sablon.</span><span class="sxs-lookup"><span data-stu-id="03295-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="03295-114">Megadhatja, hogy milyen mappa legyen az önaláírt tanúsítványok exportálásához vagy később a kulcs boltozatból való lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="03295-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="03295-115">Ha egyéni sablont és paramétert tartalmazó fájlt ad meg, nem kell megadnia a tanúsítvány adatait a paraméter-fájlban, a rendszer ezeket a paramétereket fogja kitölteni.</span><span class="sxs-lookup"><span data-stu-id="03295-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="03295-116">A négy lehetőség alább részletezve van.</span><span class="sxs-lookup"><span data-stu-id="03295-116">The four options are detailed below.</span></span> <span data-ttu-id="03295-117">Görgessen le az egyes paraméterek magyarázatához.</span><span class="sxs-lookup"><span data-stu-id="03295-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="03295-118">Példák</span><span class="sxs-lookup"><span data-stu-id="03295-118">EXAMPLES</span></span>

### <span data-ttu-id="03295-119">1. példa: csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszerét adja meg a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="03295-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="03295-120">Ez a parancs csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszert adja meg a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="03295-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="03295-121">2. példa: adjon meg egy meglévő erőforrást a kulcs-tárolóban, és egy egyéni sablon segítségével telepítsen egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="03295-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="03295-122">Ez a parancs egy meglévő tanúsítvány-erőforrást ad meg egy kulcs-tárolóban, valamint egy egyéni sablont a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="03295-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="03295-123">3. példa: új fürt létrehozása egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="03295-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="03295-124">Adja meg a kulcsfájl eltérő RG nevét, és a rendszer feltölti a tanúsítványt a rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="03295-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="03295-125">Ez a parancs egy új fürtöt hoz létre egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="03295-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="03295-126">Adja meg a kulcsfájl eltérő RG-nevét, és a rendszer feltölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="03295-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="03295-127">Példa 4: saját tanúsítvány és egyéni sablon létrehozása és új fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="03295-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="03295-128">Ezzel a paranccsal hozhatja létre saját tanúsítványát és egyéni sablonját, és létrehozhat egy új fürtöt.</span><span class="sxs-lookup"><span data-stu-id="03295-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="03295-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03295-129">PARAMETERS</span></span>

### <span data-ttu-id="03295-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="03295-130">-CertificateFile</span></span>
<span data-ttu-id="03295-131">Az elsődleges fürtcsomópont tanúsítványának meglévő elérési útja.</span><span class="sxs-lookup"><span data-stu-id="03295-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="03295-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="03295-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="03295-133">A létrehozandó új tanúsítványfájl mappája.</span><span class="sxs-lookup"><span data-stu-id="03295-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="03295-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="03295-134">-CertificatePassword</span></span>
<span data-ttu-id="03295-135">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="03295-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="03295-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="03295-136">-CertificateSubjectName</span></span>
<span data-ttu-id="03295-137">A létrehozandó tanúsítvány tulajdonosának neve.</span><span class="sxs-lookup"><span data-stu-id="03295-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="03295-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="03295-138">-ClusterSize</span></span>
<span data-ttu-id="03295-139">A fürt csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="03295-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="03295-140">Az alapértelmezett érték 5 csomópont.</span><span class="sxs-lookup"><span data-stu-id="03295-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="03295-141">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="03295-141">-KeyVaultName</span></span>
<span data-ttu-id="03295-142">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="03295-142">Azure key vault name.</span></span> <span data-ttu-id="03295-143">Ha nem adja meg, akkor a program alapértelmezés szerint az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03295-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="03295-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="03295-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="03295-145">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="03295-145">Azure key vault resource group name.</span></span> <span data-ttu-id="03295-146">Ha nem adja meg, akkor a program alapértelmezés szerint az erőforrás-csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03295-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="03295-147">-Hely</span><span class="sxs-lookup"><span data-stu-id="03295-147">-Location</span></span>
<span data-ttu-id="03295-148">Az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="03295-148">The resource group location.</span></span>

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

### <span data-ttu-id="03295-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03295-149">-Name</span></span>
<span data-ttu-id="03295-150">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="03295-150">Specify the name of the cluster.</span></span> <span data-ttu-id="03295-151">Ha nem adja meg, akkor az akkora lesz, mint az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03295-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="03295-152">-OS</span><span class="sxs-lookup"><span data-stu-id="03295-152">-OS</span></span>
<span data-ttu-id="03295-153">A fürtöt alkotó VMs operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="03295-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="03295-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="03295-154">-ParameterFile</span></span>
<span data-ttu-id="03295-155">A sablon paraméter fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="03295-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="03295-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03295-156">-ResourceGroupName</span></span>
<span data-ttu-id="03295-157">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="03295-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="03295-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="03295-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="03295-159">A másodlagos fürtcsomópont meglévő tanúsítványfájl-elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="03295-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="03295-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="03295-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="03295-161">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="03295-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="03295-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="03295-162">-SecretIdentifier</span></span>
<span data-ttu-id="03295-163">A meglévő Azure Key Vault titkos URL-címe, például: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="03295-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="03295-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="03295-164">-TemplateFile</span></span>
<span data-ttu-id="03295-165">A sablonfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="03295-165">The path to the template file.</span></span>

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

### <span data-ttu-id="03295-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="03295-166">-VmPassword</span></span>
<span data-ttu-id="03295-167">A VM jelszava.</span><span class="sxs-lookup"><span data-stu-id="03295-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="03295-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="03295-168">-VmSku</span></span>
<span data-ttu-id="03295-169">A VM SKU.</span><span class="sxs-lookup"><span data-stu-id="03295-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="03295-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="03295-170">-VmUserName</span></span>
<span data-ttu-id="03295-171">A VM-be való bejelentkezéshez használt Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="03295-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="03295-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03295-172">-Confirm</span></span>
<span data-ttu-id="03295-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03295-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03295-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03295-174">-WhatIf</span></span>
<span data-ttu-id="03295-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03295-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03295-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03295-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03295-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03295-177">-DefaultProfile</span></span>
<span data-ttu-id="03295-178">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03295-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03295-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03295-179">CommonParameters</span></span>
<span data-ttu-id="03295-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03295-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03295-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03295-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03295-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03295-182">INPUTS</span></span>

### <span data-ttu-id="03295-183">System. String</span><span class="sxs-lookup"><span data-stu-id="03295-183">System.String</span></span>
<span data-ttu-id="03295-184">System. Security. SecureString System. Int32 Microsoft. Azure. Command. ServiceFabric. models. OperatingSystem tulajdonság</span><span class="sxs-lookup"><span data-stu-id="03295-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="03295-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03295-185">OUTPUTS</span></span>

### <span data-ttu-id="03295-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="03295-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="03295-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03295-187">NOTES</span></span>

## <span data-ttu-id="03295-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03295-188">RELATED LINKS</span></span>

