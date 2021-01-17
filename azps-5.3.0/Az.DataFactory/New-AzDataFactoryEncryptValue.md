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
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Titkosítja a bizalmas adatokat.

## SZINTAXIS

### ByFactoryName (alapértelmezett)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzDataFactoryEncryptValue** parancsmag titkosítja a bizalmas adatokat, például a jelszót vagy a Microsoft SQL Server kapcsolati karakterláncát, és titkosított értéket ad vissza.

## PÉLDÁK

### 1. példa: Nem ODBC-kapcsolati karakterlánc titkosítása
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Az első parancs a ConvertTo-SecureString parancsmag segítségével **SecureString** objektumká alakítja a megadott kapcsolati karakterláncot, majd az objektumot a $Value tárolja.
További információért írja be a `Get-Help ConvertTo-SecureString` .
Engedélyezett értékek: SQL Server vagy Oracle kapcsolati karakterlánc.
A második parancs egy titkosított értéket hoz létre a $Value, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.

### 2. példa: Windows-hitelesítést használó nem ODBC-kapcsolati karakterlánc titkosítása.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Az első parancs **a ConvertTo-SecureString** paranccsal biztonságos karakterlánc-objektumká alakítja a megadott kapcsolati karakterláncot, majd tárolja az objektumot a $Value változóban.
A második parancs a Get-Credential parancsmag segítségével gyűjti össze a Windows-hitelesítést (felhasználónevet és jelszót), majd tárolja a **PSCredential** objektumot a $Credential változóban.
További információért írja be a `Get-Help Get-Credential` .
A harmadik parancs egy titkosított értéket hoz létre a $Value és $Credential tárolt objektumhoz a megadott adat-, átjáró-, erőforráscsoport- és csatolt szolgáltatástípushoz.

### 3. példa: A csatolt fájlrendszer szolgáltatás kiszolgálónevének és hitelesítő adatainak titkosítása
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Az első parancs **a ConvertTo-SecureString** paranccsal biztonságos karakterláncra konvertálja a megadott karakterláncot, majd az objektumot a $Value tárolja.
A második parancs **a Get-Credential** segítségével gyűjti össze a Windows-hitelesítést (felhasználónév és jelszó), majd tárolja a **PSCredential** objektumot a $Credential változóban.
A harmadik parancs egy titkosított értéket hoz létre a $Value és $Credential tárolt objektumhoz a megadott adat-, átjáró-, erőforráscsoport- és csatolt szolgáltatástípushoz.

### 4. példa: A CSATOLT HDFS szolgáltatás hitelesítő adatainak titkosítása
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

A **ConvertTo-SecureString** parancs biztonságos karakterláncgé alakítja a megadott karakterláncot.
A **New-Object** parancs egy PSCredential objektumot hoz létre a biztonságos felhasználónév és jelszó karakterláncok használatával.
Ehelyett a **Get-Credential** paranccsal gyűjthet Windows-hitelesítést (felhasználónév és jelszó), majd a visszaadott **PSCredential** objektumot a $credential változóban tárolhatja az előző példákban látható módon.
A **New-AzDataFactoryEncryptValue** parancs titkosított értéket hoz létre az $Credential-ban tárolt objektumhoz a megadott adatüzem, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.

### 5. példa: Az ODBC csatolt szolgáltatás hitelesítő adatainak titkosítása
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

A **ConvertTo-SecureString** parancs biztonságos karakterláncgé alakítja a megadott karakterláncot.
A **New-AzDataFactoryEncryptValue** parancs titkosított értéket hoz létre az $Value-ban tárolt objektumhoz a megadott adatüzem, átjáró, erőforráscsoport és csatolt szolgáltatástípus számára.

## PARAMETERS

### -AuthenticationType
Az adatforráshoz való csatlakozáshoz használt hitelesítés típusát határozza meg.
A paraméter elfogadható értékei a következőek:
- Windows
- Alapszintű
- Névtelen.

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

### -Hitelesítő adatok
A windowsos hitelesítési hitelesítő adatokat (felhasználónév és jelszó) adja meg.
Ez a parancsmag titkosítja az itt megadott hitelesítő adatokat.

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

### -Database
A csatolt szolgáltatás adatbázisnevét adja meg.

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

### -DataFactory
EGY **PSDataFactory-objektumot** ad meg.
Ez a parancsmag titkosítja a paraméter által megadott adat factory adatait.

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

### -DataFactoryName
Egy adatüzem nevét adja meg.
Ez a parancsmag titkosítja a paraméter által megadott adat factory adatait.

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

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -GatewayName
Az átjáró nevét adja meg.
Ez a parancsmag titkosítja a paraméter által megadott átjáró adatait.

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

### -NonCredentialValue
Az ODBC-kapcsolati karakterlánc nem hitelesítő adatokkal kapcsolatos részét adja meg.
Ez a paraméter csak az ODBC csatolt szolgáltatásra vonatkozik.

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

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag a paraméter által megadott csoport adatait titkosítja.

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

### -Server
A csatolt szolgáltatás kiszolgálónevét adja meg.

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

### -Type
A csatolt szolgáltatás típusát adja meg.
Ez a parancsmag titkosítja a paraméter által megadott csatolt szolgáltatástípus adatait.
A paraméter elfogadható értékei a következőek:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

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

### -Érték
A titkosítja az értéket.
Egy helyszíni SQL Serverhez csatolt szolgáltatás és egy helyszíni Oracle-csatolt szolgáltatás esetén használjon kapcsolati karakterláncot.
Helyszíni ODBC-csatolt szolgáltatás esetén használja a kapcsolati karakterlánc hitelesítőadat-részét.
Helyszíni fájlrendszerhez kapcsolt szolgáltatás esetén, ha a fájlrendszer helyi az átjáró számítógépére, használja a Local vagy localhost szolgáltatást, és ha a fájlrendszer az átjárót kiszolgálótól eltérő kiszolgálón található, használja a \\ \\ kiszolgálónevet.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## KIMENETEK

### System.String

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


