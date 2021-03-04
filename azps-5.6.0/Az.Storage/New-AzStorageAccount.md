---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939849"
---
# New-AzStorageAccount

## SYNOPSIS
Tárfiókot hoz létre.

## SZINTAXIS

### AzureActiveDirectoryDomainServicesForFile (alapértelmezett)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageAccount** parancsmag létrehoz egy Azure Storage-fiókot.

## PÉLDÁK

### 1. példa: Tárfiók létrehozása
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Ez a parancs tárfiókot hoz létre a MyResourceGroup nevű erőforráscsoporthoz.

### 2. példa: Blob-tárfiók létrehozása BlobStorage típusú és gyors AccessTier-fiókkal
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Ezzel a paranccsal olyan Blob Storage-fiókot hoz létre, amely blobstorage típusú és gyors AccessTier típusú

### 3. példa: Tárfiók létrehozása a Kind StorageV2 segítségével, valamint identitás létrehozása és hozzárendelése az Azure KeyVaulthoz.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Ez a parancs létrehoz egy Tárfiókot a Kind StorageV2 segítségével.  Emellett létrehoz és hozzárendel egy identitást, amely a fiókkulcsok Azure KeyVaulton keresztüli kezelésére használható.

### 4. példa: Tárfiók létrehozása a NetworkRuleSet segítségével a JSON-ból
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Ez a parancs egy Olyan tárfiókot hoz létre, amely a JSON-ból NetworkRuleSet tulajdonságot hoz létre

### 5. példa: Tárfiók létrehozása engedélyezett Hierarchikus névtér funkcióval.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Ez a parancs egy tárfiókot hoz létre, és a Hierarchikus névtér engedélyezve van.

### 6. példa: Hozzon létre egy tárfiókot az Azure Files AAD DS-hitelesítéssel, és engedélyezze a nagy fájlmegosztást.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Ez a parancs létrehoz egy Tárfiókot az Azure Files AAD DS Authentication segítségével, és engedélyezi a nagy fájlmegosztást.

### 7. példa: Tárfiók létrehozása a Files Active Directory tartományi szolgáltatás hitelesítésének engedélyezésével.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Ez a parancs egy tárolófiókot hoz létre, amely tartalmazza az Active Directory tartományi szolgáltatások hitelesítését.

### 8. példa: Tárfiók létrehozása a várólistával és a táblaszolgáltatással fiókfedő titkosítási kulcsot, valamint infrastruktúra-titkosítás megkövetelése.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

Ez a parancs létrehoz egy tárfiókot a Várólistával és a Táblaszolgáltatással, és fiókfüggvényes titkosítási kulcsot használ, és infrastruktúra-titkosítást igényel, így a várólistán és a táblázatban ugyanaz a titkosítási kulcs fog használni a Blob és a Fájl szolgáltatással, és a szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal az adatokhoz.
Ezután szerezze be a Tárfiók tulajdonságait, és tekintse meg a Várólistás és a Táblaszolgáltatás titkosítási kulcstípusát, valamint a RequireInfrastructureEncryption értéket.

### 9. példa: Fiók minimumTlsVersion és AllowBlobPublicAccess létrehozása és a SharedKey Access letiltása
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

A parancs a MinimumTlsVersion, az AllowBlobPublicAccess és a SharedKey hozzáférés letiltása a fiókhoz, majd a létrehozott fiók 3 tulajdonságának megjelenítése 

### 10. példa: Tárfiók létrehozása a RoutingPreference beállítással
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

Ez a parancs létrehoz egy Tárfiókot a RoutingPreference beállítással: a PublishMicrosoftEndpoint és a PublishInternetEndpoint mint true, a RoutingChoice pedig MicrosoftRouting.

## PARAMETERS

### -AccessTier
A parancsmag által létrehozott tárfiók hozzáférési rétegét adja meg.
A paraméter elfogadható értékei a következőek: Hot és Cool.
Ha a Kind paraméterhez blobstorage értéket ad meg, meg kell adnia az  *AccessTier paraméter értékét.* Ha a Kind paraméterhez  tárterületértéket ad meg, ne adja meg az *AccessTier paramétert.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Az Azure Storage biztonsági azonosítóját (SID) adja meg. Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
A tartomány GUID azonosítóját adja meg. Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Azt az elsődleges tartományt adja meg, amely esetén az AD DNS-kiszolgáló mérvadó. Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Megadja a biztonsági azonosítót (SID). Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
A lekért Active Directory-erdőt határozza meg. Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetNamesDomainName
A Net ROSTAS tartománynevét adja meg. Ezt a paramétert akkor kell beállítani, ha az -EnableActiveDirectoryDomainServicesForFile értéke igaz.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
Nyilvános hozzáférés engedélyezése a tárfiók összes blobját vagy tárolóját. A tulajdonság alapértelmezett értelmezése igaz.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSharedKeyAccess
Azt jelzi, hogy a tárfiók engedélyezi-e a fiók hozzáférési kulcsával való engedély kérését a Megosztott kulcson keresztül. Ha hamis, akkor minden kérést engedélyezni kell az Azure Active Directory (Azure AD) használatával, beleértve a megosztott hozzáférés-aláírásokat is. Az alapértelmezett érték null, amely egyenértékű az igaz értékkel.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Hozzon létre és rendeljen hozzá egy új tárfiók-identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDomainName
A Tárfiók egyéni tartományának nevét adja meg.
Az alapértelmezett érték a Tárterület.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -EnableActiveDirectoryDomainServicesForFile
Engedélyezze az Azure Files Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
Engedélyezze az Azure Files Azure Active Directory tartományi szolgáltatás hitelesítését a tárfiókhoz.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Azt jelzi, hogy a Tárfiók engedélyezi-e a hierarchikus névteret.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Azt jelzi, hogy a Tárfiók csak https-forgalmat tesz-e lehetővé.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Azt jelzi, hogy a tárfiók támogatja-e az 5 TiB-kapacitásnál nagyobb fájlmegosztásokat. A fiók engedélyezése után a funkció nem tiltható le. Jelenleg csak az LRS és a ZRS replikációs típusai támogatottak, ezért a fiókok georedundáns fiókokra konvertálása nem lenne lehetséges. További információ: https://go.microsoft.com/fwlink/?linkid=2086047

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForQueue
Állítsa be a várólistán lévő titkosítási kulcstípust. Az alapértelmezett érték a Szolgáltatás.
-Fiók: A várólistát fiókható titkosítási kulccsal titkosítja a rendszer. -Szolgáltatás: A várólistát a rendszer mindig titkos kulcsokkal Service-Managed titkosítja. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
Állítsa be a táblázat titkosítási kulcstípusát. Az alapértelmezett érték a Szolgáltatás.
- Fiók: A tábla fiókható titkosítási kulccsal lesz titkosítva. 
- Szolgáltatás: A tábla mindig titkosítva lesz a Service-Managed kulcsokkal. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Meghatározza, hogy a parancsmag milyen típusú tárfiókot hoz létre.
A paraméter elfogadható értékei a következőek:
- Tárterület. Általános célú tárfiók, amely támogatja a blobok, táblák, várólisták, fájlok és lemezek tárolását.
- StorageV2. Általános célú 2-es verzió (GPv2) tárfiók, amely támogatja a blobokat, a táblákat, a várólistákat, a fájlokat és a lemezeket speciális funkciókkal, például adatrétegezéssel.
- BlobStorage. Blob storage account which supports storage of Blobs only.
- BlockBlobStorage. Letilthatja a Blob Storage-fiókot, amely csak a blokk blobok tárolását támogatja.
- FileStorage. Fájltárfiók, amely csak a fájlok tárolását támogatja.
Az alapértelmezett érték a StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Megadja a létrehozni szükséges tárfiók helyét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
A tárterület-kérelmek esetén megengedett minimális TLS-verzió. A tulajdonság alapértelmezett értelmezése a TLS 1.0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A létrehozni szükséges tárfiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé térő szolgáltatások értékeinek beállítására, valamint a megadott szabályoktól különböző kérések kezelésére használható.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishInternetEndpoint
Azt jelzi, hogy közzé kell-e tenni az internetes útválasztási tárolási végpontokat

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishMicrosoftEndpoint
Azt jelzi, hogy közzé kell-e tenni a Microsoft útválasztási tár végpontját

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireInfrastructureEncryption
A szolgáltatás egy másodlagos titkosítási réteget alkalmaz platform felügyelt kulcsokkal a nyugta adatokhoz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelyhez hozzá kell adni a Tárfiókot.

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

### -RoutingChoice
Az Útválasztási választási lehetőség a felhasználó által választott hálózati útválasztási típust határozza meg. Lehetséges értékek: "MicrosoftRouting", "InternetRouting"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
A parancsmag által létrehozott tárfiók termékváltozatnevét adja meg.
A paraméter elfogadható értékei a következőek:
- Standard_LRS. Helyileg redundáns tárterület.
- Standard_ZRS. Zone-redundáns tárterület.
- Standard_GRS. Georedundáns tárterület.
- Standard_RAGRS. Georedundáns tárterület olvasása.
- Premium_LRS. Prémium helyileg redundáns tárterület.
- Premium_ZRS. Prémium zóna redundáns tárterület.
- Standard_GZRS – Georedundáns zónaredundáns tárolás.
- Standard_RAGZRS – Olvassa el a georedundáns zóna-redundáns tárhelyet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Azt jelzi, hogy engedélyezi-e a CName közvetett érvényesítését.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
