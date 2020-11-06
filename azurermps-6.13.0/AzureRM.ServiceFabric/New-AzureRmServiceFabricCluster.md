---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 87fb451028fb0e345bd8748573424cf33066e52b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502903"
---
# <span data-ttu-id="43a6c-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="43a6c-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="43a6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="43a6c-103">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="43a6c-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="43a6c-104">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="43a6c-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="43a6c-105">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="43a6c-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a6c-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43a6c-106">SYNTAX</span></span>

### <span data-ttu-id="43a6c-107">ByDefaultArmTemplate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43a6c-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a6c-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="43a6c-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a6c-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="43a6c-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a6c-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="43a6c-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43a6c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="43a6c-111">DESCRIPTION</span></span>
<span data-ttu-id="43a6c-112">A **New-AzureRmServiceFabricCluster** parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványok segítségével új szolgáltatási szövet típusú fürtöt állíthat be.</span><span class="sxs-lookup"><span data-stu-id="43a6c-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="43a6c-113">A használt sablon lehet egy alapértelmezett sablon vagy egy Ön által megadott egyéni sablon.</span><span class="sxs-lookup"><span data-stu-id="43a6c-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="43a6c-114">Megadhatja, hogy milyen mappa legyen az önaláírt tanúsítványok exportálásához vagy később a kulcs boltozatból való lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="43a6c-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="43a6c-115">Ha egyéni sablont és paramétert tartalmazó fájlt ad meg, nem kell megadnia a tanúsítvány adatait a paraméter-fájlban, a rendszer ezeket a paramétereket fogja kitölteni.</span><span class="sxs-lookup"><span data-stu-id="43a6c-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="43a6c-116">A négy lehetőség alább részletezve van.</span><span class="sxs-lookup"><span data-stu-id="43a6c-116">The four options are detailed below.</span></span> <span data-ttu-id="43a6c-117">Görgessen le az egyes paraméterek magyarázatához.</span><span class="sxs-lookup"><span data-stu-id="43a6c-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="43a6c-118">Példák</span><span class="sxs-lookup"><span data-stu-id="43a6c-118">EXAMPLES</span></span>

### <span data-ttu-id="43a6c-119">1. példa: csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszerét adja meg a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="43a6c-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="43a6c-120">Ez a parancs csak a szektorcsoport méretét, a tanúsítvány tárgyát és az operációs rendszert adja meg a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="43a6c-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="43a6c-121">2. példa: adjon meg egy meglévő erőforrást a kulcs-tárolóban, és egy egyéni sablon segítségével telepítsen egy fürtöt.</span><span class="sxs-lookup"><span data-stu-id="43a6c-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="43a6c-122">Ez a parancs egy meglévő tanúsítvány-erőforrást ad meg egy kulcs-tárolóban, valamint egy egyéni sablont a fürt központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="43a6c-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="43a6c-123">3. példa: új fürt létrehozása egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="43a6c-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="43a6c-124">Adjon meg egy másik erőforráscsoport-nevet a kulcsfájl számára, és a rendszer feltölt egy új tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="43a6c-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="43a6c-125">Ez a parancs egy új fürtöt hoz létre egyéni sablon használatával.</span><span class="sxs-lookup"><span data-stu-id="43a6c-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="43a6c-126">Adjon meg egy másik erőforráscsoport-nevet a kulcsfájl számára, és a rendszer feltölt egy új tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="43a6c-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="43a6c-127">Példa 4: saját tanúsítvány és egyéni sablon létrehozása és új fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="43a6c-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="43a6c-128">Ezzel a paranccsal hozhatja létre saját tanúsítványát és egyéni sablonját, és létrehozhat egy új fürtöt.</span><span class="sxs-lookup"><span data-stu-id="43a6c-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="43a6c-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43a6c-129">PARAMETERS</span></span>

### <span data-ttu-id="43a6c-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="43a6c-130">-CertificateFile</span></span>
<span data-ttu-id="43a6c-131">Az elsődleges fürtcsomópont tanúsítványának meglévő elérési útja.</span><span class="sxs-lookup"><span data-stu-id="43a6c-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="43a6c-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="43a6c-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="43a6c-133">A létrehozandó új tanúsítványfájl mappája.</span><span class="sxs-lookup"><span data-stu-id="43a6c-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="43a6c-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="43a6c-134">-CertificatePassword</span></span>
<span data-ttu-id="43a6c-135">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="43a6c-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="43a6c-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="43a6c-136">-CertificateSubjectName</span></span>
<span data-ttu-id="43a6c-137">A létrehozandó tanúsítvány tulajdonosának neve.</span><span class="sxs-lookup"><span data-stu-id="43a6c-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="43a6c-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="43a6c-138">-ClusterSize</span></span>
<span data-ttu-id="43a6c-139">A fürt csomópontjainak száma.</span><span class="sxs-lookup"><span data-stu-id="43a6c-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="43a6c-140">Az alapértelmezett érték 5 csomópont.</span><span class="sxs-lookup"><span data-stu-id="43a6c-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="43a6c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a6c-141">-DefaultProfile</span></span>
<span data-ttu-id="43a6c-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43a6c-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a6c-143">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="43a6c-143">-KeyVaultName</span></span>
<span data-ttu-id="43a6c-144">Azure Key Vault-név</span><span class="sxs-lookup"><span data-stu-id="43a6c-144">Azure key vault name.</span></span> <span data-ttu-id="43a6c-145">Ha nem adja meg, akkor a program alapértelmezés szerint az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43a6c-145">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="43a6c-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a6c-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="43a6c-147">Azure Key Vault-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="43a6c-147">Azure key vault resource group name.</span></span> <span data-ttu-id="43a6c-148">Ha nem adja meg, akkor a program alapértelmezés szerint az erőforrás-csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43a6c-148">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="43a6c-149">-Hely</span><span class="sxs-lookup"><span data-stu-id="43a6c-149">-Location</span></span>
<span data-ttu-id="43a6c-150">Az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="43a6c-150">The resource group location.</span></span>

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

### <span data-ttu-id="43a6c-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43a6c-151">-Name</span></span>
<span data-ttu-id="43a6c-152">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="43a6c-152">Specify the name of the cluster.</span></span> <span data-ttu-id="43a6c-153">Ha nem adja meg, akkor az akkora lesz, mint az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43a6c-153">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="43a6c-154">-OS</span><span class="sxs-lookup"><span data-stu-id="43a6c-154">-OS</span></span>
<span data-ttu-id="43a6c-155">A fürtöt alkotó VMs operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="43a6c-155">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="43a6c-156">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="43a6c-156">-ParameterFile</span></span>
<span data-ttu-id="43a6c-157">A sablon paraméter fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="43a6c-157">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="43a6c-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a6c-158">-ResourceGroupName</span></span>
<span data-ttu-id="43a6c-159">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="43a6c-159">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="43a6c-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="43a6c-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="43a6c-161">A másodlagos fürtcsomópont meglévő tanúsítványfájl-elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="43a6c-161">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="43a6c-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="43a6c-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="43a6c-163">A tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="43a6c-163">The password of the certificate file.</span></span>

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

### <span data-ttu-id="43a6c-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="43a6c-164">-SecretIdentifier</span></span>
<span data-ttu-id="43a6c-165">A meglévő Azure Key Vault titkos URL-címe, például: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="43a6c-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="43a6c-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="43a6c-166">-TemplateFile</span></span>
<span data-ttu-id="43a6c-167">A sablonfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="43a6c-167">The path to the template file.</span></span>

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

### <span data-ttu-id="43a6c-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="43a6c-168">-VmPassword</span></span>
<span data-ttu-id="43a6c-169">A VM jelszava.</span><span class="sxs-lookup"><span data-stu-id="43a6c-169">The password of the Vm.</span></span>

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

### <span data-ttu-id="43a6c-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="43a6c-170">-VmSku</span></span>
<span data-ttu-id="43a6c-171">A VM SKU.</span><span class="sxs-lookup"><span data-stu-id="43a6c-171">The Vm Sku.</span></span>

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

### <span data-ttu-id="43a6c-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="43a6c-172">-VmUserName</span></span>
<span data-ttu-id="43a6c-173">A VM-be való bejelentkezéshez használt Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="43a6c-173">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="43a6c-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43a6c-174">-Confirm</span></span>
<span data-ttu-id="43a6c-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43a6c-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a6c-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a6c-176">-WhatIf</span></span>
<span data-ttu-id="43a6c-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43a6c-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43a6c-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43a6c-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a6c-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a6c-179">CommonParameters</span></span>
<span data-ttu-id="43a6c-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43a6c-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a6c-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a6c-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a6c-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a6c-182">INPUTS</span></span>

### <span data-ttu-id="43a6c-183">System. String</span><span class="sxs-lookup"><span data-stu-id="43a6c-183">System.String</span></span>
<span data-ttu-id="43a6c-184">Paraméterek: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), Location (ByValue), Name (ByValue), ParameterFile (ByValue), SecondaryCertificateFile (ByValue), SecretIdentifier (ByValue), TemplateFile (ByValue), VmUserName (ByValue), (), ()</span><span class="sxs-lookup"><span data-stu-id="43a6c-184">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), Location (ByValue), Name (ByValue), ParameterFile (ByValue), SecondaryCertificateFile (ByValue), SecretIdentifier (ByValue), TemplateFile (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="43a6c-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="43a6c-185">System.Security.SecureString</span></span>
<span data-ttu-id="43a6c-186">Paraméterek: CertificatePassword (ByValue), SecondaryCertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43a6c-186">Parameters: CertificatePassword (ByValue), SecondaryCertificatePassword (ByValue)</span></span>

### <span data-ttu-id="43a6c-187">System. Int32</span><span class="sxs-lookup"><span data-stu-id="43a6c-187">System.Int32</span></span>
<span data-ttu-id="43a6c-188">Paraméterek: ClusterSize (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43a6c-188">Parameters: ClusterSize (ByValue)</span></span>

### <span data-ttu-id="43a6c-189">Microsoft. Azure. Command. ServiceFabric. models. OperatingSystem tulajdonság</span><span class="sxs-lookup"><span data-stu-id="43a6c-189">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="43a6c-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43a6c-190">OUTPUTS</span></span>

### <span data-ttu-id="43a6c-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="43a6c-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="43a6c-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43a6c-192">NOTES</span></span>

## <span data-ttu-id="43a6c-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43a6c-193">RELATED LINKS</span></span>
