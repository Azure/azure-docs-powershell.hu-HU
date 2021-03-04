---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921546"
---
# Get-AzSynapseSqlPoolGeoBackup

## SYNOPSIS
Geodundáns biztonsági másolatot készít egy Sql-készletről.

## SZINTAXIS

### GetByNameParameterSet (alapértelmezett)
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SqlPoolGeoBackupResourceId
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzSynapseSqlPoolGeoBackup** parancsmag meghatározott georedundáns biztonsági másolatot kap egy SQL-készletről vagy egy adott munkaterületen rendelkezésre álló georedundáns biztonsági másolatról.
A georedundáns biztonsági másolat egy különálló földrajzi helyről származó adatfájlokat használó visszaállítható erőforrás.
A Geo-Restore segítségével visszaállíthat egy georedundáns biztonsági másolatot, ha egy regionális kimaradás miatt az SQL-készletet visszaállítja egy új régióba.

## PÉLDÁK

### 1. példa: Meghatározott georedundáns biztonsági másolat készítése
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
A parancsmag beolvassa a Geo Backup függvényt egy sql-készlethez.

### 2. példa: Az összes georedundáns biztonsági másolat lekérte egy munkaterületre
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
Ez a parancs minden földrajzi redundáns biztonsági mentést elérhetővé válik egy adott munkaterületen.

### 3. példa: Az összes georedundáns biztonsági másolat behozása egy munkaterületre szűréssel
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
Ez a parancs a "Contoso" kezdetű adott munkaterületen elérhető georedundáns biztonsági másolatokat kap.

## PARAMETERS

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

### -Name
A Synapse Sql-készlet.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Sql Pool Geo Backup Resource Id bevitele.

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
A Synapse-munkaterület neve.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## KIMENETEK

### Microsoft.Azure.Commands.Synapse.Models.PSBackupModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
