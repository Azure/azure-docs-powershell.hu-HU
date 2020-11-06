---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 5de4c34281b2122880a683f070e771dc15d93c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502996"
---
# <span data-ttu-id="68e57-101">New-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="68e57-101">New-AzureRmDataFactoryEncryptValue</span></span>

## <span data-ttu-id="68e57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68e57-102">SYNOPSIS</span></span>
<span data-ttu-id="68e57-103">A bizalmas adatokat titkosítja.</span><span class="sxs-lookup"><span data-stu-id="68e57-103">Encrypts sensitive data.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68e57-104">SYNTAX</span></span>

### <span data-ttu-id="68e57-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68e57-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68e57-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="68e57-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68e57-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="68e57-107">DESCRIPTION</span></span>
<span data-ttu-id="68e57-108">A **New-AzureRmDataFactoryEncryptValue** parancsmag titkosítja a bizalmas adatokat, például jelszót vagy Microsoft SQL Server-kapcsolati karakterláncot, és a titkosított értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="68e57-108">The **New-AzureRmDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="68e57-109">Példák</span><span class="sxs-lookup"><span data-stu-id="68e57-109">EXAMPLES</span></span>

### <span data-ttu-id="68e57-110">Példa 1: nem ODBC kapcsolatú karakterlánc titkosítása</span><span class="sxs-lookup"><span data-stu-id="68e57-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="68e57-111">Az első parancs az ConvertTo-SecureString parancsmagot használja a megadott kapcsolati karakterlánc **SecureString** -objektummá alakításához, majd az objektumot a $Value változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="68e57-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="68e57-112">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="68e57-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="68e57-113">Engedélyezett értékek: SQL Server vagy Oracle-kapcsolati karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="68e57-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="68e57-114">A második parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol a megadott Data Factory, Gateway, erőforráscsoport és a kapcsolt szolgáltatás típusa esetén.</span><span class="sxs-lookup"><span data-stu-id="68e57-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="68e57-115">2. példa: titkosítson egy nem ODBC kapcsolatú karakterláncot, amely a Windows-hitelesítést használja.</span><span class="sxs-lookup"><span data-stu-id="68e57-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="68e57-116">Az első parancs a **ConvertTo-SecureString** használatával konvertálja a megadott kapcsolati karakterláncot egy biztonságos karakterlánc-objektumra, majd a $Value változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="68e57-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="68e57-117">A második parancs a Get-Credential parancsmagot használja a Windows-hitelesítés (Felhasználónév és jelszó) összegyűjtéséhez, majd a **PSCredential** objektum tárolása a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="68e57-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="68e57-118">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="68e57-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="68e57-119">A harmadik parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol, és $Credential a megadott Data Factory, Gateway, erőforráscsoport és kapcsolt szolgáltatás típusa esetén.</span><span class="sxs-lookup"><span data-stu-id="68e57-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="68e57-120">3. példa: a kiszolgáló nevének és hitelesítő adatainak titkosítása a fájlrendszerhez kapcsolt szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="68e57-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="68e57-121">Az első parancs a **ConvertTo-SecureString** használatával konvertálja a megadott karakterláncot egy biztonságos karakterláncba, majd a $Value változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="68e57-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="68e57-122">A második parancs a **Get-hitelesítő adatokkal** gyűjti össze a Windows-hitelesítést (felhasználónevet és jelszót), majd a **PSCredential** objektumot a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="68e57-122">The second command uses **Get-Credential** to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="68e57-123">A harmadik parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol, és $Credential a megadott Data Factory, Gateway, erőforráscsoport és kapcsolt szolgáltatás típusa esetén.</span><span class="sxs-lookup"><span data-stu-id="68e57-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="68e57-124">Példa 4: a HDFS-hoz kapcsolt szolgáltatás hitelesítő adatainak titkosítása</span><span class="sxs-lookup"><span data-stu-id="68e57-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="68e57-125">A **ConvertTo-SecureString** parancs egy biztonságos karakterláncba konvertálja a megadott karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="68e57-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="68e57-126">A **New-Object** parancs a biztonságos Felhasználónév és a jelszó karakterlánc segítségével hoz létre PSCredential-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="68e57-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="68e57-127">Ehelyett használhatja a **Get-hitelesítőadat** parancsot a Windows-hitelesítés (Felhasználónév és jelszó) összegyűjtéséhez, majd a visszaadott **PSCredential** objektum tárolásához a $Credential változóban, az előző példákban látható módon.</span><span class="sxs-lookup"><span data-stu-id="68e57-127">Instead, you could use the **Get-Credential** command to collect windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="68e57-128">A **New-AzureRmDataFactoryEncryptValue** parancs létrehoz egy titkosított értéket az $Credential-ban tárolt objektumhoz a megadott adatgyári, átjáró, erőforráscsoport és kapcsolt szolgáltatás típusához.</span><span class="sxs-lookup"><span data-stu-id="68e57-128">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="68e57-129">5. példa: hitelesítő adatok titkosítása az ODBC-hez kapcsolt szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="68e57-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="68e57-130">A **ConvertTo-SecureString** parancs egy biztonságos karakterláncba konvertálja a megadott karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="68e57-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="68e57-131">A **New-AzureRmDataFactoryEncryptValue** parancs létrehoz egy titkosított értéket az $Value-ban tárolt objektumhoz a megadott adatgyári, átjáró, erőforráscsoport és kapcsolt szolgáltatás típusához.</span><span class="sxs-lookup"><span data-stu-id="68e57-131">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="68e57-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68e57-132">PARAMETERS</span></span>

### <span data-ttu-id="68e57-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="68e57-133">-AuthenticationType</span></span>
<span data-ttu-id="68e57-134">Az adatforráshoz való csatlakozáshoz használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="68e57-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="68e57-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68e57-136">Windows</span><span class="sxs-lookup"><span data-stu-id="68e57-136">Windows</span></span>
- <span data-ttu-id="68e57-137">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="68e57-137">Basic</span></span>
- <span data-ttu-id="68e57-138">Névtelen.</span><span class="sxs-lookup"><span data-stu-id="68e57-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-139">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="68e57-139">-Credential</span></span>
<span data-ttu-id="68e57-140">A használni kívánt Windows-hitelesítési hitelesítő adatok (Felhasználónév és jelszó) meghatározása.</span><span class="sxs-lookup"><span data-stu-id="68e57-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="68e57-141">Ez a parancsmag titkosítja az itt megadott hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="68e57-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-142">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="68e57-142">-Database</span></span>
<span data-ttu-id="68e57-143">A kapcsolt szolgáltatás adatbázisának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="68e57-144">-DataFactory</span></span>
<span data-ttu-id="68e57-145">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="68e57-146">Ez a parancsmag titkosítja az adatfeldolgozó adattípusát, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="68e57-147">-DataFactoryName</span></span>
<span data-ttu-id="68e57-148">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="68e57-149">Ez a parancsmag titkosítja az adatfeldolgozó adattípusát, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e57-150">-DefaultProfile</span></span>
<span data-ttu-id="68e57-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68e57-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68e57-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="68e57-152">-GatewayName</span></span>
<span data-ttu-id="68e57-153">Az átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="68e57-154">Ez a parancsmag titkosítja az adatot a paraméter által megadott átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="68e57-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="68e57-155">-NonCredentialValue</span></span>
<span data-ttu-id="68e57-156">Az Open Database Connectivity (ODBC) kapcsolati karakterlánc nem hitelesítő részét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="68e57-157">Ez a paraméter csak az ODBC-alapú kapcsolt szolgáltatásban használható.</span><span class="sxs-lookup"><span data-stu-id="68e57-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e57-158">-ResourceGroupName</span></span>
<span data-ttu-id="68e57-159">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68e57-160">Ez a parancsmag titkosítja azokat az adatcsoportokat, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-161">-Server</span><span class="sxs-lookup"><span data-stu-id="68e57-161">-Server</span></span>
<span data-ttu-id="68e57-162">A kapcsolt szolgáltatás kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-163">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="68e57-163">-Type</span></span>
<span data-ttu-id="68e57-164">A kapcsolt szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-164">Specifies the linked service type.</span></span>
<span data-ttu-id="68e57-165">Ez a parancsmag a kapcsolt szolgáltatás típusának értékét titkosítja, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="68e57-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="68e57-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68e57-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="68e57-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="68e57-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="68e57-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="68e57-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="68e57-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="68e57-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="68e57-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="68e57-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="68e57-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-176">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="68e57-176">-Value</span></span>
<span data-ttu-id="68e57-177">A titkosítani kívánt értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e57-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="68e57-178">Ha egy helyszíni SQL Server-alapú kapcsolt szolgáltatáshoz és egy helyszíni Oracle-alapú szolgáltatáshoz kapcsolódik, használja a kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="68e57-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="68e57-179">Helyszíni ODBC-csatolású szolgáltatás esetén használja a kapcsolati karakterlánc hitelesítő részét.</span><span class="sxs-lookup"><span data-stu-id="68e57-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="68e57-180">A helyszíni fájlrendszerhez kapcsolt szolgáltatás esetén, ha a fájlrendszer helyi az átjáró számítógépén van, használja a helyi vagy a localhost értéket, és ha a fájlrendszer az átjárótól eltérő kiszolgálón található, használja a \\ \\ kiszolgálónév nevet.</span><span class="sxs-lookup"><span data-stu-id="68e57-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e57-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e57-181">CommonParameters</span></span>
<span data-ttu-id="68e57-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68e57-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e57-183">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e57-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e57-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e57-184">INPUTS</span></span>

### <span data-ttu-id="68e57-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="68e57-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="68e57-186">System. String</span><span class="sxs-lookup"><span data-stu-id="68e57-186">System.String</span></span>

## <span data-ttu-id="68e57-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e57-187">OUTPUTS</span></span>

### <span data-ttu-id="68e57-188">System. String</span><span class="sxs-lookup"><span data-stu-id="68e57-188">System.String</span></span>

## <span data-ttu-id="68e57-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68e57-189">NOTES</span></span>
* <span data-ttu-id="68e57-190">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="68e57-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="68e57-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68e57-191">RELATED LINKS</span></span>

[<span data-ttu-id="68e57-192">Új – AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="68e57-192">New-AzureRmDataFactoryEncryptValue</span></span>](./New-AzureRmDataFactoryEncryptValue.md)

