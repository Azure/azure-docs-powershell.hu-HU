---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015823"
---
# Set-AzureRoute

## Áttekintés
Útvonalat hoz létre az útvonal-táblában.

## SZINTAXISA

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureRoute** parancsmag útvonalat hoz létre egy útvonal-táblában.
Az új útvonal szinte azonnal életbe lép az útválasztási táblázathoz társított virtuális gépeken.

## Példák

### Példa 1: virtuális készülék felvétele következő ugrási útvonalon
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

A parancs létrehoz egy ApplianceRouteTable nevű útvonalkártya-táblázatot a megadott helyen.
A parancs átadja az útválasztási táblázatot az aktuális parancsmagnak.
Az aktuális parancsmag hozzáadja a ApplianceRoute03 nevű útvonalat, amely a következő ugrás típusú VirtualAppliance.
A parancs a következő ugrási IP-címet és az útvonalhoz tartozó cím előtagot adja meg.

### 2. példa: az Internet következő ugrási útvonalának felvétele
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Ez a parancs a ApplianceRouteTable nevű útválasztási táblázatot kapja.
A parancs átadja az útválasztási táblázatot az aktuális parancsmagnak.
Az aktuális parancsmag hozzáadja a InternetRoute nevű útvonalat, amely egy internetes következő ugrás típusú.
A parancs az útvonalhoz tartozó cím előtagját adja meg.

## PARAMÉTEREK

### -AddressPrefix
Az új útvonalhoz tartozó cím előtagját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
Annak a készüléknek az IP-címét adja meg, amely az útvonalat használó forgalom következő ugrása.
Ezt az értéket csak akkor adja meg, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopType
Az útvonalat használó forgalom következő ugrási típusát adja meg.
Az érvényes értékek a következők: 

- VPNGateway
- VNETLocal
- Internet
- VirtualAppliance
- NULL

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -RouteName
A parancsmag által hozzáadott új útvonal nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RouteTable
Annak az útvonalnak a táblázatát adja meg, amelyre a parancsmag hozzáadja az új útvonalat.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRoute](./Remove-AzureRoute.md)


