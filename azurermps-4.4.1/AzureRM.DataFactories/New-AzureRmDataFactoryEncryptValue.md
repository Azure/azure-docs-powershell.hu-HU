---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 54a759370f39dcd3844d42d858d23f6c178a4d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672706"
---
# New-AzureRmDataFactoryEncryptValue

## Áttekintés
A bizalmas adatokat titkosítja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmDataFactoryEncryptValue** parancsmag titkosítja a bizalmas adatokat, például jelszót vagy Microsoft SQL Server-kapcsolati karakterláncot, és a titkosított értéket adja eredményül.

## Példák

### Példa 1: nem ODBC kapcsolatú karakterlánc titkosítása
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Az első parancs az ConvertTo-SecureString parancsmagot használja a megadott kapcsolati karakterlánc **SecureString** -objektummá alakításához, majd az objektumot a $Value változóban tárolja.
További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .
Engedélyezett értékek: SQL Server vagy Oracle-kapcsolati karakterlánc.

A második parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol a megadott Data Factory, Gateway, erőforráscsoport és a kapcsolt szolgáltatás típusa esetén.

### 2. példa: titkosítson egy nem ODBC kapcsolatú karakterláncot, amely a Windows-hitelesítést használja.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

Az első parancs a **ConvertTo-SecureString** használatával konvertálja a megadott kapcsolati karakterláncot egy biztonságos karakterlánc-objektumra, majd a $Value változóban tárolja az objektumot.

A második parancs a Get-Credential parancsmagot használja a Windows-hitelesítés (Felhasználónév és jelszó) összegyűjtéséhez, majd a **PSCredential** objektum tárolása a $Credential változóban.
További információért írja be a következőt: `Get-Help Get-Credential` .

A harmadik parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol, és $Credential a megadott Data Factory, Gateway, erőforráscsoport és kapcsolt szolgáltatás típusa esetén.

### 3. példa: a kiszolgáló nevének és hitelesítő adatainak titkosítása a fájlrendszerhez kapcsolt szolgáltatáshoz
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Az első parancs a **ConvertTo-SecureString** használatával konvertálja a megadott karakterláncot egy biztonságos karakterláncba, majd a $Value változóban tárolja az objektumot.

A második parancs a **Get-hitelesítő adatokkal** gyűjti össze a Windows-hitelesítést (felhasználónevet és jelszót), majd a **PSCredential** objektumot a $Credential változóban tárolja.

A harmadik parancs létrehoz egy titkosított értéket az objektumhoz, amelyet az $Value tárol, és $Credential a megadott Data Factory, Gateway, erőforráscsoport és kapcsolt szolgáltatás típusa esetén.

### Példa 4: a HDFS-hoz kapcsolt szolgáltatás hitelesítő adatainak titkosítása
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

A **ConvertTo-SecureString** parancs egy biztonságos karakterláncba konvertálja a megadott karakterláncot.
A **New-Object** parancs a biztonságos Felhasználónév és a jelszó karakterlánc segítségével hoz létre PSCredential-objektumokat.
Ehelyett használhatja a **Get-hitelesítőadat** parancsot a Windows-hitelesítés (Felhasználónév és jelszó) összegyűjtéséhez, majd a visszaadott **PSCredential** objektum tárolásához a $Credential változóban, az előző példákban látható módon.

A **New-AzureRmDataFactoryEncryptValue** parancs létrehoz egy titkosított értéket az $Credential-ban tárolt objektumhoz a megadott adatgyári, átjáró, erőforráscsoport és kapcsolt szolgáltatás típusához.

### 5. példa: hitelesítő adatok titkosítása az ODBC-hez kapcsolt szolgáltatáshoz
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

A **ConvertTo-SecureString** parancs egy biztonságos karakterláncba konvertálja a megadott karakterláncot.

A **New-AzureRmDataFactoryEncryptValue** parancs létrehoz egy titkosított értéket az $Value-ban tárolt objektumhoz a megadott adatgyári, átjáró, erőforráscsoport és kapcsolt szolgáltatás típusához.

## PARAMÉTEREK

### -AuthenticationType
Az adatforráshoz való csatlakozáshoz használt hitelesítés típusát adja meg.
A paraméter elfogadható értékei a következők:

- Windows
- Egyszerű
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
A használni kívánt Windows-hitelesítési hitelesítő adatok (Felhasználónév és jelszó) meghatározása.
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

### -Database (adatbázis)
A kapcsolt szolgáltatás adatbázisának nevét adja meg.

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
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag titkosítja az adatfeldolgozó adattípusát, amely ezt a paramétert adja meg.

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
Az adatfeldolgozó nevét adja meg.
Ez a parancsmag titkosítja az adatfeldolgozó adattípusát, amely ezt a paramétert adja meg.

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

### -GatewayName
Az átjáró nevét adja meg.
Ez a parancsmag titkosítja az adatot a paraméter által megadott átjáróhoz.

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

### -NonCredentialValue
Az Open Database Connectivity (ODBC) kapcsolati karakterlánc nem hitelesítő részét adja meg.
Ez a paraméter csak az ODBC-alapú kapcsolt szolgáltatásban használható.

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
Ez a parancsmag titkosítja azokat az adatcsoportokat, amelyeket ez a paraméter határoz meg.

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
A kapcsolt szolgáltatás kiszolgálójának nevét adja meg.

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

### -Type (típus)
A kapcsolt szolgáltatás típusát adja meg.
Ez a parancsmag a kapcsolt szolgáltatás típusának értékét titkosítja, amelyet a paraméter határoz meg.
A paraméter elfogadható értékei a következők:

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

### -Value (érték)
A titkosítani kívánt értéket adja meg.
Ha egy helyszíni SQL Server-alapú kapcsolt szolgáltatáshoz és egy helyszíni Oracle-alapú szolgáltatáshoz kapcsolódik, használja a kapcsolati karakterláncot.
Helyszíni ODBC-csatolású szolgáltatás esetén használja a kapcsolati karakterlánc hitelesítő részét.
A helyszíni fájlrendszerhez kapcsolt szolgáltatás esetén, ha a fájlrendszer helyi az átjáró számítógépén van, használja a helyi vagy a localhost értéket, és ha a fájlrendszer az átjárótól eltérő kiszolgálón található, használja a \\ \\ kiszolgálónév nevet.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. String

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


