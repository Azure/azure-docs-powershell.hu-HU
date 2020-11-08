---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195102"
---
# Get-AzMySqlConnectionString

## Áttekintés
A kapcsolati karakterlánc beszerzése az ügyfél-kapcsolat szolgáltatója szerint.

## SZINTAXISA

### Get (alapértelmezett)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Leírás
A kapcsolati karakterlánc beszerzése az ügyfél-kapcsolat szolgáltatója szerint.

## Példák

### 1. példa: a MySql-kiszolgáló kapcsolódási karakterláncának beszerzése erőforráscsoport szerint erőforráscsoport és kiszolgálónév szerint
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

Ez a parancsmag a MySql Server Connection karakterláncot az erőforráscsoport és a kiszolgáló neve alapján kapja meg.

### 2. példa: a MySql-kiszolgáló kapcsolati karakterláncának beolvasása identitással
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

Ez a parancsmag identitással kapja meg a MySql Server Connection karakterláncot.

## PARAMÉTEREK

### -Client
Ügyfél-kapcsolat szolgáltatója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A Source Server objektum a replika létrehozásához.
A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A kiszolgáló neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az Azure-előfizetést azonosító előfizetési azonosító.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. MySql. models. Api20171201. IServer

## KIMENETEK

### System. String

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <IServer> : a Source Server objektum, amelyből replika hozható létre.
  - `Location <String>`: Az a hely, ahol az erőforrás tartózkodik.
  - `[Tag <ITrackedResourceTags>]`: Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[AdministratorLogin <String>]`: A rendszergazda bejelentkezési neve a kiszolgálón. Csak a kiszolgáló létrehozásakor (és a létrehozáshoz szükséges) lehet megadni.
  - `[EarliestRestoreDate <DateTime?>]`: A legkorábbi visszaállítási pont létrehozási ideje (ISO8601 formátum)
  - `[FullyQualifiedDomainName <String>]`: A kiszolgáló teljesen minősített tartományneve.
  - `[IdentityType <IdentityType?>]`: Az identitás típusa. A "SystemAssigned" beállítással automatikusan létrehozhatja és hozzárendelheti az erőforráshoz az Azure Active Directory-beli megbízót.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Állapot, amelyen látható, hogy a kiszolgáló engedélyezve van-e az infrastruktúra titkosítása.
  - `[MasterServerId <String>]`: A replikakészlet kiszolgálói azonosítója.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Minimális TLS-verzió érvényesítése a kiszolgálón.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: A kiszolgálón engedélyezve van-e a nyilvános hálózatokhoz való hozzáférés. Az érték nem kötelező, de ha be van kapcsolva, "engedélyezve" vagy "Letiltva" állapotban kell lennie.
  - `[ReplicaCapacity <Int32?>]`: A főkiszolgáló által használható replikák maximális száma.
  - `[ReplicationRole <String>]`: A kiszolgáló replikációs szerepköre.
  - `[SkuCapacity <Int32?>]`: A méret fel/ki kapacitás, amely a kiszolgáló számítási egységeit jelképezi.
  - `[SkuFamily <String>]`: A hardver családja.
  - `[SkuName <String>]`: A SKU neve (általában a Tier + család + magok), például B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Az erőforrás által a megfelelő módon értelmezhető dimenziókód.
  - `[SkuTier <SkuTier?>]`: Az adott SKU Tier (például alap).
  - `[SslEnforcement <SslEnforcementEnum?>]`: Engedélyezze az SSL-kényszerítést, vagy ne a kiszolgálóhoz való csatlakozáskor.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Biztonsági adatmegőrzési napok a kiszolgálón.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: A tárterület automatikus bővülésének engedélyezése
  - `[StorageProfileStorageMb <Int32?>]`: Maximális tárterület a kiszolgálón.
  - `[UserVisibleState <ServerState?>]`: Egy olyan kiszolgáló állapota, amely látható a felhasználó számára.
  - `[Version <ServerVersion?>]`: Kiszolgáló verziója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

