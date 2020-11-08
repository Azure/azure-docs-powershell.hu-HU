---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016045"
---
# Set-AzureVMChefExtension

## Áttekintés
Hozzáadja a séf bővítményt a virtuális géphez.

## SZINTAXISA

### Windows (alapértelmezett)
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureVMChefExtension** parancsmag hozzáadja a Chef bővítményt a virtuális géphez.

## Példák

### 1. példa: Chef-kiterjesztés hozzáadása Windows Virtual Machine-géphez
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

A parancs hozzáadja a Chef bővítményt a Windows Virtual Machine programhoz.
Amikor a virtuális gép jön létre, a bootstrapped a séf, és az Apache-ot futtatja.

### 2. példa: a Chef Extension bővítmény felvétele Windows Virtual Machine-be a rendszerindítás során
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

Ez a parancs hozzáadja a Chef bővítményt egy Windows Virtual Machine programhoz.
Amikor elindul a virtuális gép, a bootstrapped a séf futtatja, és az Apache-ot futtatja.
A rendszerindítás után a virtuális gép a JSON formátumban megadott *BootstrapOptions* hivatkozik.

### 3. példa: Chef-kiterjesztés felvétele Windows Virtual Machine-be, és telepítése az Apache és a GIT segítségével
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

Ez a parancs hozzáadja a Chef bővítményt egy Windows Virtual Machine programhoz.
Amikor elindul a virtuális gép, bootstrapped a séf, és telepítve van az Apache és a GIT.
Ha nem adja meg az Client. RB, meg kell adni a séf-kiszolgáló URL-címét és az érvényesítési ügyfél nevét.

### 4. példa: Chef-kiterjesztés hozzáadása egy linuxos virtuális géphez
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

Ez a parancs hozzáadja a Chef bővítményt egy linuxos virtuális géphez.
Amikor elindul a virtuális gép, az a séf bootstrapped van.
Ha nem ad meg ügyfelet. RB, meg kell adni a séf-kiszolgáló URL-címét és szervezetét.

## PARAMÉTEREK

### -BootstrapOptions
A betöltési beállításokat a JavaScript-objektumokhoz (JSON) tartalmazó formátumban adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BootstrapVersion
A Chef ügyfélprogramnak a kiterjesztéssel együtt telepített verzióját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ChefDaemonInterval
Annak gyakoriságát adja meg (percben), amikor a séf-szolgáltatás fut. Ha abban az esetben, ha nem szeretné, hogy a séf-szolgáltatás telepítve legyen az Azure VM-ben, akkor ebben a mezőben a 0 értéket adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ChefServerUrl
A séf-kiszolgáló URL-címét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRb
A Chef Client. RB teljes elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Daemon
A Chef-Client szolgáltatás beállítása felügyelet nélküli végrehajtáshoz. A csomópont platformjának Windows rendszernek kell lennie.
Engedélyezett beállítások: "nincs", "szolgáltatás" és "tevékenység".
nincs – ez a beállítás megakadályozza a Chef-Client szolgáltatás szolgáltatásként való konfigurálását.
szolgáltatás – beállítja a séf – ügyfelet, hogy szolgáltatásként automatikusan fusson a háttérben.
feladat – úgy állítja be a Chef-clientt, hogy automatikusan fusson a háttérben secheduled tevékenységként.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonAttribute
A Chef-Client első futtatásához hozzáadni kívánt JSON-karakterlánc. például-JsonAttribute ' {"foo": "sáv"} '

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Jelzi, hogy ez a parancsmag egy Linux-beli virtuális gépet hoz létre.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szervezetnév
A séf-kiterjesztés szervezeti nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunList
A Chef Node Run (sorozat) lista.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcs.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecretFile
Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcsot tartalmazó fájl elérési útja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidationClientName
Az érvényesítési ügyfél nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidationPem
A Chef validator. PEM fájl elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A séf-kiterjesztés verziószámát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Az állandó virtuálisgép-objektumot adja meg.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVMChefExtension](./Get-AzureVMChefExtension.md)

[Remove-AzureVMChefExtension](./Remove-AzureVMChefExtension.md)


