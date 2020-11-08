---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183806"
---
# New-AzStorageAccount

## Áttekintés
Tároló fiókot hoz létre.

## SZINTAXISA

### AzureActiveDirectoryDomainServicesForFile (alapértelmezett)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.

## Példák

### Példa 1: tárterület-fiók létrehozása
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.

### 2. példa: blob-tároló létrehozása a BlobStorage-féle és a forró AccessTier
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Ez a parancs olyan blob-tárterületet hoz létre, amely BlobStorage típusú és forró AccessTier

### 3. példa: hozzon létre egy Kind StorageV2 tároló fiókot, és hozzon létre és rendeljen identitást az Azure.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Ez a parancs a Kind StorageV2 létrehoz egy tárterület-fiókot.  Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.

### Példa 4: a NetworkRuleSet származó tárhely-fiók létrehozása a JSON-ról
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Ez a parancs létrehoz egy olyan tárolási fiókot, amely a NetworkRuleSet tulajdonságot tartalmazza a JSON-ról

### Példa 5: tárterület-fiók létrehozása a hierarchikus névtér engedélyezve értékkel.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Ez a parancs létrehoz egy olyan tárterület-fiókot, amelyben a hierarchikus névtér engedélyezve van.

### 6. példa: hozzon létre egy tárterületet az Azure-fájlokkal AAD DS-hitelesítéssel, és engedélyezze a nagyméretű fájlok megosztását.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Ez a parancs létrehoz egy olyan tárterület-fiókot, amely Azure-fájlokat AAD a DS-hitelesítéshez, és lehetővé teszi a nagyméretű fájlok megosztását.

### 7. példa: hozzon létre egy tárolási fiókot, és engedélyezze a fájlok Active Directory tartományi szolgáltatás hitelesítését.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Ez a parancs létrehoz egy tárolási fiókot withenable-fájlok Active Directory tartományi szolgáltatás-hitelesítéssel.

### 8. példa: a várólista-és a táblázat-szolgáltatási tárterület létrehozásakor fiók-hatókörű titkosítási kulccsal kell rendelkezniük, és infrastrukturális titkosítást kell használniuk.
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

Ez a parancs létrehoz egy tárolási fiókot a várólistával és a táblázat szolgáltatással, és a fiók hatókörű titkosítási kulcsát használja, és infrastruktúra-titkosítást igényel, ezért a várólista és a táblázat ugyanazzal a titkosítási kulccsal fog rendelkezni, mint a blob és a fájlkezelő, valamint a szolgáltatás a többszintű adatok platformon kezelt kulcsait alkalmazza.
Ezután kapja meg a tárolási fiók tulajdonságait, és tekintse meg a várólista és a táblázat szolgáltatás titkosítási típusát, valamint a RequireInfrastructureEncryption értékét.

### 9. példa: fiók MinimumTlsVersion és AllowBlobPublicAccess létrehozása
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

A parancs létrehoz egy fiókot a MinimumTlsVersion és a AllowBlobPublicAccess, majd megjeleníti a létrehozott fiók 2 tulajdonságát. 

## PARAMÉTEREK

### -AccessTier
A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.
A paraméter elfogadható értékei a következők: meleg és hűvös.
Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét. Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.

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
Az Azure-tárterület biztonsági azonosítóját adja meg. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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
A tartomány GUID-azonosítóját adja meg. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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
Annak az elsődleges tartománynak a megadása, amelyhez az AD DNS-kiszolgáló mérvadó. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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
A biztonsági azonosítót (SID) adja meg. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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
A beolvasott Active Directory-erdőt adja meg. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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

### -ActiveDirectoryNetBiosDomainName
A NetBIOS-tartománynevet adja meg. Ezt a paramétert akkor adja meg, ha a-EnableActiveDirectoryDomainServicesForFile igaz értékre van állítva.

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
Engedélyezze a nyilvános hozzáférést a tárterülethez tartozó összes blobhoz vagy tárolóhoz. A tulajdonság alapértelmezett értelmezése igaz.

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
A parancsmag futtatása a háttérben

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
Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.

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
A tárolási fiók egyéni tartományának nevét adja meg.
Az alapértelmezett érték a tárterület.

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
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Engedélyezze az Azure-fájlok Active Directory tartományi szolgáltatás-hitelesítését a tárterület-fiókhoz.

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
Engedélyezze az Azure-fájlok Azure Active Directory tartományi szolgáltatás általi hitelesítését a tárolási fiókhoz.

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
Azt jelzi, hogy a tárolási fiók engedélyezi-e a hierarchikus névteret.

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
Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.

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
Azt jelzi, hogy a tárolási fiók támogatja-e az 5 TiB-nál több kapacitással rendelkező nagyméretű fájlmegosztás használatát. Miután a fiók engedélyezve van, a funkció nem tiltható le. Jelenleg csak a LRS és a ZRS replikációs típusai támogatottak, ezért nem lehetett beírni a "geo-redundáns fiókok" konverzióját. További információ https://go.microsoft.com/fwlink/?linkid=2086047

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
Állítsa be a várólista titkosítási típusát. Az alapértelmezett érték a szolgáltatás.
-Fiók: a várólista a fiók hatókörű titkosítási kulccsal lesz titkosítva. -Szolgáltatás: a várólista mindig Service-Managed kulcsokkal lesz titkosítva. 

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
Állítsa be a tábla titkosítási típusát. Az alapértelmezett érték a szolgáltatás.
- Fiók: a tábla a fiókhoz tartozó titkosítási kulccsal lesz titkosítva. 
- Szolgáltatás: a táblázat Service-Managed billentyűvel mindig titkosítva lesz. 

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
A parancsmag által létrehozott tárolási fiók típusát adja meg.
A paraméter elfogadható értékei a következők:
- Tárterület. Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.
- StorageV2. Általános célú 2-es verzió (GPv2) tárterülete, melyen a festékfoltok, a táblázatok, a várólisták, a fájlok és a lemezek a speciális funkciók, például az adatrétegek támogatása.
- BlobStorage. BLOB-tároló fiók, amely támogatja a BLOB-tárolót.
- BlockBlobStorage. A blob-tároló fiók zárolása, amely támogatja a csak blokkos Blobok tárolását.
- FileStorage. A csak a fájlok tárterületét támogató fájl-tároló fiók.
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

### -Hely
A létrehozandó tárterület-fiók helyét adja meg.

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
A tárolási kérelmeken engedélyezni kívánt minimális TLS-verzió. Az alapértelmezett értelmezés a TLS 1,0 tulajdonság.

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

### -Name (név)
A létrehozandó tárterület-fiók nevét adja meg.

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
A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.

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

### -RequireInfrastructureEncryption
A szolgáltatás másodlagos titkosítási réteget alkalmaz a REST-alapú adatok platformon kezelt kulcsaival.

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
Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.

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

### -SkuName
Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.
A paraméter elfogadható értékei a következők:
- Standard_LRS. Helyileg redundáns tárterület.
- Standard_ZRS. Zóna – redundáns tárterület.
- Standard_GRS. Geo-redundáns tárterület.
- Standard_RAGRS. Olvassa el az Access geo-redundáns tárterülete című témakört.
- Premium_LRS. Prémium lokálisan redundáns tárterület.
- Premium_ZRS. Prémium zóna – redundáns tárterület.
- Standard_GZRS-geo-redundáns zóna – redundáns tárterület.
- Standard_RAGZRS – az Access geo-redundáns zónája – redundáns tárterület.

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

### -Címke
A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

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
Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
