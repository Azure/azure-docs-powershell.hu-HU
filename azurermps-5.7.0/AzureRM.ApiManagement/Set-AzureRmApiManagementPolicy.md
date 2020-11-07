---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672660"
---
# Set-AzureRmApiManagementPolicy

## Áttekintés
Az API-kezeléshez megadott hatóköri házirend beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### SetTenantLevel (alapértelmezett)
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetProductLevel
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetApiLevel
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetOperationLevel
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmApiManagementPolicy** PARANCSMAG az API-kezeléshez megadott hatóköri házirendet állítja be.

## Példák

### Példa 1: a bérlői szint házirendjének beállítása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

Ez a parancs a bérlői szintű házirendet egy tenantpolicy.xml nevű fájlból állítja be.

### 2. példa: termékspecifikus házirend beállítása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

Ez a parancs az API-kezeléshez tartozó termékspecifikus házirendet állítja be.

### 3. példa: API-scope-házirend beállítása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

Ez a parancs az API-menedzsment API-hatóköri házirendjét állítja be.

### 4. példa: a műveleti tartomány házirendjének beállítása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

Ez a parancs beállítja az API-kezeléshez szükséges műveleti hatóköri házirendet.

## PARAMÉTEREK

### -ApiId
A meglévő API azonosítóját adja meg.
Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet állítja be.

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
A **PsApiManagementContext** példányát adja meg.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Formátumú
A házirend formátumát adja meg.
Az alapértelmezett érték az "Application/vnd. MS-Azure-APIM. Policy + XML".

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

### -OperationId
A meglévő művelet azonosítóját adja meg.
Ha a ApiId megadásakor a művelet hatóköre házirendet adja meg.
Ehhez a paraméterekre van szükség.

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Házirend
A házirend-dokumentumot karakterláncként adja meg.
Ez a paraméter akkor szükséges, ha a- *PolicyFilePath* nincs megadva.

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

### -PolicyFilePath
A házirendfájl elérési útját adja meg.
Ez a paraméter akkor szükséges, ha a *házirend* paraméter nincs megadva.

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

### -Termékkód
A meglévő szorzat azonosítóját adja meg.
Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet állítja be.

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### bool

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Remove-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)


