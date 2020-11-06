---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493294"
---
# Get-AzureRmApiManagementBackend

## Áttekintés
Ismerje meg a backend részleteit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### GetAllBackends (alapértelmezett)
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByBackendId
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Ismerje meg a backend részleteit.

## Példák

### Példa 1: az összes backend beolvasása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

Az API-kezelési szolgáltatásban konfigurált összes backend-elem listáját kapja.

### 2. példa: a 123 azonosítóval megadott backend beolvasása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

A "123" azonosítóval azonosított megadott backend részleteinek megjelenítése

## PARAMÉTEREK

### -BackendId
A backend-azonosító.
Ha meg van adva, a program megpróbálja megtalálni a backend-et az azonosítóval.
Ez a paraméter nem kötelező.

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
A PsApiManagementContext példánya.
Ehhez a paraméterhez szükség van.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend
Az API-kezelési szolgáltatásban konfigurált backend részletei.

### IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend>
Az API-kezelési szolgáltatásban konfigurált backend-lista.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmApiManagementBackend](./New-AzureRmApiManagementBackend.md)

[Új – AzureRmApiManagementBackendCredential](./New-AzureRmApiManagementBackendCredential.md)

[Új – AzureRmApiManagementBackendProxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[Remove-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)
