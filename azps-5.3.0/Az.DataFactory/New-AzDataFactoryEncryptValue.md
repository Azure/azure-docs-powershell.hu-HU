---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477133"
---
# <span data-ttu-id="e98e4-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="e98e4-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="e98e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e98e4-103">Titkosítja a bizalmas adatokat.</span><span class="sxs-lookup"><span data-stu-id="e98e4-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="e98e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e98e4-104">SYNTAX</span></span>

### <span data-ttu-id="e98e4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e98e4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98e4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e98e4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e98e4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e98e4-107">DESCRIPTION</span></span>
<span data-ttu-id="e98e4-108">A **New-AzDataFactoryEncryptValue** parancsmag titkosítja a bizalmas adatokat, például a jelszót vagy a Microsoft SQL Server kapcsolati karakterláncát, és titkosított értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="e98e4-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="e98e4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e98e4-109">EXAMPLES</span></span>

### <span data-ttu-id="e98e4-110">1. példa: Nem ODBC-kapcsolati karakterlánc titkosítása</span><span class="sxs-lookup"><span data-stu-id="e98e4-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="e98e4-111">Az első parancs a ConvertTo-SecureString parancsmag segítségével **SecureString** objektumká alakítja a megadott kapcsolati karakterláncot, majd az objektumot a $Value tárolja.</span><span class="sxs-lookup"><span data-stu-id="e98e4-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="e98e4-112">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e98e4-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e98e4-113">Engedélyezett értékek: SQL Server vagy Oracle kapcsolati karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="e98e4-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="e98e4-114">A második parancs egy titkosított értéket hoz létre a $Value, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.</span><span class="sxs-lookup"><span data-stu-id="e98e4-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="e98e4-115">2. példa: Windows-hitelesítést használó nem ODBC-kapcsolati karakterlánc titkosítása.</span><span class="sxs-lookup"><span data-stu-id="e98e4-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="e98e4-116">Az első parancs **a ConvertTo-SecureString** paranccsal biztonságos karakterlánc-objektumká alakítja a megadott kapcsolati karakterláncot, majd tárolja az objektumot a $Value változóban.</span><span class="sxs-lookup"><span data-stu-id="e98e4-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="e98e4-117">A második parancs a Get-Credential parancsmag segítségével gyűjti össze a Windows-hitelesítést (felhasználónevet és jelszót), majd tárolja a **PSCredential** objektumot a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="e98e4-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="e98e4-118">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e98e4-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="e98e4-119">A harmadik parancs egy titkosított értéket hoz létre a $Value és $Credential tárolt objektumhoz a megadott adat-, átjáró-, erőforráscsoport- és csatolt szolgáltatástípushoz.</span><span class="sxs-lookup"><span data-stu-id="e98e4-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="e98e4-120">3. példa: A csatolt fájlrendszer szolgáltatás kiszolgálónevének és hitelesítő adatainak titkosítása</span><span class="sxs-lookup"><span data-stu-id="e98e4-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="e98e4-121">Az első parancs **a ConvertTo-SecureString** paranccsal biztonságos karakterláncra konvertálja a megadott karakterláncot, majd az objektumot a $Value tárolja.</span><span class="sxs-lookup"><span data-stu-id="e98e4-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="e98e4-122">A második parancs **a Get-Credential** segítségével gyűjti össze a Windows-hitelesítést (felhasználónév és jelszó), majd tárolja a **PSCredential** objektumot a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="e98e4-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="e98e4-123">A harmadik parancs egy titkosított értéket hoz létre a $Value és $Credential tárolt objektumhoz a megadott adat-, átjáró-, erőforráscsoport- és csatolt szolgáltatástípushoz.</span><span class="sxs-lookup"><span data-stu-id="e98e4-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="e98e4-124">4. példa: A CSATOLT HDFS szolgáltatás hitelesítő adatainak titkosítása</span><span class="sxs-lookup"><span data-stu-id="e98e4-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="e98e4-125">A **ConvertTo-SecureString** parancs biztonságos karakterláncgé alakítja a megadott karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="e98e4-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="e98e4-126">A **New-Object** parancs egy PSCredential objektumot hoz létre a biztonságos felhasználónév és jelszó karakterláncok használatával.</span><span class="sxs-lookup"><span data-stu-id="e98e4-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="e98e4-127">Ehelyett a **Get-Credential** paranccsal gyűjthet Windows-hitelesítést (felhasználónév és jelszó), majd a visszaadott **PSCredential** objektumot a $credential változóban tárolhatja az előző példákban látható módon.</span><span class="sxs-lookup"><span data-stu-id="e98e4-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="e98e4-128">A **New-AzDataFactoryEncryptValue** parancs titkosított értéket hoz létre az $Credential-ban tárolt objektumhoz a megadott adatüzem, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.</span><span class="sxs-lookup"><span data-stu-id="e98e4-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="e98e4-129">5. példa: Az ODBC csatolt szolgáltatás hitelesítő adatainak titkosítása</span><span class="sxs-lookup"><span data-stu-id="e98e4-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="e98e4-130">A **ConvertTo-SecureString** parancs biztonságos karakterláncgé alakítja a megadott karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="e98e4-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="e98e4-131">A **New-AzDataFactoryEncryptValue** parancs titkosított értéket hoz létre az $Value-ban tárolt objektumhoz a megadott adatüzem, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.</span><span class="sxs-lookup"><span data-stu-id="e98e4-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="e98e4-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98e4-132">PARAMETERS</span></span>

### <span data-ttu-id="e98e4-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e98e4-133">-AuthenticationType</span></span>
<span data-ttu-id="e98e4-134">Az adatforráshoz való csatlakozáshoz használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="e98e4-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="e98e4-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e98e4-136">Windows</span><span class="sxs-lookup"><span data-stu-id="e98e4-136">Windows</span></span>
- <span data-ttu-id="e98e4-137">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="e98e4-137">Basic</span></span>
- <span data-ttu-id="e98e4-138">Névtelen.</span><span class="sxs-lookup"><span data-stu-id="e98e4-138">Anonymous.</span></span>

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

### <span data-ttu-id="e98e4-139">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="e98e4-139">-Credential</span></span>
<span data-ttu-id="e98e4-140">A windowsos hitelesítési hitelesítő adatokat (felhasználónév és jelszó) adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="e98e4-141">Ez a parancsmag titkosítja az itt megadott hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e98e4-141">This cmdlet encrypts the credential data you specify here.</span></span>

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

### <span data-ttu-id="e98e4-142">-Database</span><span class="sxs-lookup"><span data-stu-id="e98e4-142">-Database</span></span>
<span data-ttu-id="e98e4-143">A csatolt szolgáltatás adatbázisnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-143">Specifies the database name of the linked service.</span></span>

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

### <span data-ttu-id="e98e4-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e98e4-144">-DataFactory</span></span>
<span data-ttu-id="e98e4-145">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e98e4-146">Ez a parancsmag titkosítja a paraméter által megadott adat factory adatait.</span><span class="sxs-lookup"><span data-stu-id="e98e4-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e98e4-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e98e4-147">-DataFactoryName</span></span>
<span data-ttu-id="e98e4-148">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e98e4-149">Ez a parancsmag titkosítja a paraméter által megadott adat factory adatait.</span><span class="sxs-lookup"><span data-stu-id="e98e4-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e98e4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98e4-150">-DefaultProfile</span></span>
<span data-ttu-id="e98e4-151">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e98e4-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e98e4-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="e98e4-152">-GatewayName</span></span>
<span data-ttu-id="e98e4-153">Az átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="e98e4-154">Ez a parancsmag titkosítja a paraméter által megadott átjáró adatait.</span><span class="sxs-lookup"><span data-stu-id="e98e4-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e4-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="e98e4-155">-NonCredentialValue</span></span>
<span data-ttu-id="e98e4-156">Az ODBC-kapcsolati karakterlánc nem hitelesítő adatokkal kapcsolatos részét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="e98e4-157">Ez a paraméter csak az ODBC csatolt szolgáltatásra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e98e4-157">This parameter is applicable only for the ODBC linked service.</span></span>

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

### <span data-ttu-id="e98e4-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e98e4-158">-ResourceGroupName</span></span>
<span data-ttu-id="e98e4-159">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e98e4-160">Ez a parancsmag a paraméter által megadott csoport adatait titkosítja.</span><span class="sxs-lookup"><span data-stu-id="e98e4-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e98e4-161">-Server</span><span class="sxs-lookup"><span data-stu-id="e98e4-161">-Server</span></span>
<span data-ttu-id="e98e4-162">A csatolt szolgáltatás kiszolgálónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-162">Specifies the server name of the linked service.</span></span>

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

### <span data-ttu-id="e98e4-163">-Type</span><span class="sxs-lookup"><span data-stu-id="e98e4-163">-Type</span></span>
<span data-ttu-id="e98e4-164">A csatolt szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98e4-164">Specifies the linked service type.</span></span>
<span data-ttu-id="e98e4-165">Ez a parancsmag titkosítja a paraméter által megadott csatolt szolgáltatástípus adatait.</span><span class="sxs-lookup"><span data-stu-id="e98e4-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="e98e4-166">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="e98e4-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e98e4-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="e98e4-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="e98e4-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="e98e4-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="e98e4-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="e98e4-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="e98e4-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="e98e4-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="e98e4-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="e98e4-175">OnPremisesSybaseLinkedService</span></span>

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

### <span data-ttu-id="e98e4-176">-Érték</span><span class="sxs-lookup"><span data-stu-id="e98e4-176">-Value</span></span>
<span data-ttu-id="e98e4-177">A titkosítja az értéket.</span><span class="sxs-lookup"><span data-stu-id="e98e4-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="e98e4-178">Egy helyszíni SQL Serverhez csatolt szolgáltatás és egy helyszíni Oracle-csatolt szolgáltatás esetén használjon kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="e98e4-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="e98e4-179">Helyszíni ODBC-csatolt szolgáltatás esetén használja a kapcsolati karakterlánc hitelesítőadat-részét.</span><span class="sxs-lookup"><span data-stu-id="e98e4-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="e98e4-180">Helyszíni fájlrendszerhez kapcsolt szolgáltatás esetén, ha a fájlrendszer helyi az átjáró számítógépére, használja a Local vagy localhost szolgáltatást, és ha a fájlrendszer az átjárót kiszolgálótól eltérő kiszolgálón található, használja a \\ \\ kiszolgálónevet.</span><span class="sxs-lookup"><span data-stu-id="e98e4-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

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

### <span data-ttu-id="e98e4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98e4-181">CommonParameters</span></span>
<span data-ttu-id="e98e4-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98e4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98e4-183">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e98e4-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98e4-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e98e4-184">INPUTS</span></span>

### <span data-ttu-id="e98e4-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e98e4-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e98e4-186">System.String</span><span class="sxs-lookup"><span data-stu-id="e98e4-186">System.String</span></span>

## <span data-ttu-id="e98e4-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e98e4-187">OUTPUTS</span></span>

### <span data-ttu-id="e98e4-188">System.String</span><span class="sxs-lookup"><span data-stu-id="e98e4-188">System.String</span></span>

## <span data-ttu-id="e98e4-189">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e98e4-189">NOTES</span></span>
* <span data-ttu-id="e98e4-190">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="e98e4-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e98e4-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e98e4-191">RELATED LINKS</span></span>

[<span data-ttu-id="e98e4-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="e98e4-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


