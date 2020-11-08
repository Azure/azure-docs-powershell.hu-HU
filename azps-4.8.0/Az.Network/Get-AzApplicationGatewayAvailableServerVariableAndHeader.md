---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025223"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## Áttekintés
A támogatott kiszolgálói változók és a rendelkezésre álló kérések és válaszok fejlécének beszerzése.

## SZINTAXISA

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## Leírás
A **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag a támogatott kiszolgálói változókat és a rendelkezésre álló kérések és válaszok fejlécét kapja. A változók és a fejlécek listájának beszerzéséhez használható paraméterek.

## Példák

### Példa 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Ez a parancs az összes elérhető kiszolgálói változót visszaállítja.

### 2. példa
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Ez a parancs az összes rendelkezésre álló kérés fejlécét visszaállítja.

### 3. példa
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Ez a parancs az összes elérhető válasz fejlécét visszaállítja.

### 4. példa
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Ez a parancs az összes elérhető kiszolgálói változót, kérést és válasz fejlécet visszaadja.

### Példa 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Ez a parancs az összes elérhető kiszolgálói változót, kérést és válasz fejlécet visszaadja.

## PARAMÉTEREK

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

### -RequestHeader
Az Application Gateway elérhető kérések fejlécei.

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

### -ResponseHeader
Az alkalmazás-átjáró elérhető válasz fejléce.

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

### -ServerVariable
Az alkalmazás-átjáró elérhető kiszolgálói változói.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## MEGJEGYZI
**Lista – a AzApplicationGatewayAvailableServerVariableAndHeader** a **Get-AzApplicationGatewayAvailableServerVariableAndHeader** parancsmag aliasa.

## KAPCSOLÓDÓ HIVATKOZÁSOK
