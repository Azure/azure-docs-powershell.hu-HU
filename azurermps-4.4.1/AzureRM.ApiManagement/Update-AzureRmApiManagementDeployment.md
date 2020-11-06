---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492588"
---
# Update-AzureRmApiManagementDeployment

## Áttekintés
Frissíti az API-kezelési szolgáltatás telepítését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Adott API-kezelési szolgáltatás (alapértelmezett)
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Frissítés a PsApiManagement-példányról
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Update-AzureRmApiManagementDeployment** parancsmag FRISSÍTI az API-kezelési szolgáltatás aktuális telepített példányait.

## Példák

### Példa 1: egy ApiManagement példány telepített példányának frissítése
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

Ez a parancs frissíti az API-kezelési példányok három egységnyi kapacitású szabványba való bevezetését.

### 2. példa: ApiManagement-példány beszerzése és átméretezése
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

Ebben a példában egy API-kezelési példány válik, és öt prémium egységre méretezi, majd egy további három egységet ad hozzá a prémium régióhoz.

### 3. példa: a frissítés telepítése (külső VNET)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

Ez a parancs frissíti egy meglévő API-kezelési telepítőt, és csatlakozik egy külső *VpnType*.

### 4. példa: a frissítés telepítése (belső VNET)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

Ez a parancs frissíti egy meglévő API-kezelési üzembe állítást, és csatlakozik egy belső *VpnType*.

## PARAMÉTEREK

### -AdditionalRegions
Az Azure API-menedzsment további központi terjesztési területeit adja meg.

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiManagement
Azt a **PsApiManagement** -példányt adja meg, amelyből beolvassa a telepítő konfigurációját.
Akkor használja ezt a paramétert, ha a példány már rendelkezik az összes szükséges módosítással.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapacitás
Itt adhatja meg az Azure API-alapú központi telepítő terület SKU-kapacitását.

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
A fő API-kezelés központi központi telepítéséhez használható terület helyét adja meg.

A paraméter elfogadható értékei a következők:

- Közép-amerikai Észak-amerikai
- Dél-Közép-amerikai
- Közép-amerikai
- Nyugat-Európa
- Észak-Európa
- Nyugat-amerikai
- Kelet-amerikai
- Kelet-amerikai 2
- Japán (kelet)
- Japán West
- Dél-Brazília
- Dél-ázsiai
- Kelet-ázsiai
- Ausztrália – Kelet
- Ausztrália délkeleti

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A parancsmag által frissített API-kezelés nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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
Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Itt adhatja meg az Azure API-kezelés központi központi telepítéséhez tartozó terület rétegét.

A paraméter elfogadható értékei a következők:

- Fejlesztő
- Standard
- Prémium verzió

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
A fő Azure API-kezelési terület virtuális hálózati konfigurációját adja meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Az API-kezelés központi telepítését megadó virtuális hálózati típust adja meg.
A paraméter elfogadható értékei a következők:

- Nincs.
Az API-kezelés bevezetése nem része bármely virtuális hálózatnak.
Ez az alapértelmezett érték. 
- Külső.
Az API-kezelés bevezetésének külső virtuális címe van. 
- Belső.
Az API-kezelés központi központi elérési környezete intranetes virtuális címet tartalmaz.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### PsApiManagement
A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagement

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)


