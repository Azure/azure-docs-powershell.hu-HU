---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 8e93847c3a6d993c689d0ac8c40327ddfcbe76af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502552"
---
# New-AzureRmMlOpCluster

## Áttekintés
Új operationalization-fürtöt hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### CreateWithInputObject
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateWithParameters
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Új operationalization-fürtöt hoz létre. Ezzel létrehoz egy cluster objektumot, egy tároló szolgáltatást, ha szükséges, az alkalmazások és az Azure Container beállításjegyzéke.

## Példák

### Példa 1
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

Új operationalization-fürtöt hoz létre az Azure Container Service és a Kubernetes Orchestrator.

### 2. példa
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

Új operationalization-fürtöt hoz létre helyben. Ezzel létrehoz egy Azure Container-nyilvántartót, az alkalmazások elemzését és a tárolási fiókot, de nem hoz létre tároló szolgáltatást.

## PARAMÉTEREK

### -AgentCount
Az ügynök csomópontjainak száma az ACS-fürtben.

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgentVmSize
Az ügynök csomópontjainak száma az ACS-fürtben.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContainerRegistry
A létrehozása helyett az Azure Container beállításjegyzékének URI-azonosítója.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId
Az ACS-fürt Orchestrator-szolgáltatásának fő azonosítója.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
A operationalization típusa.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Leírás
A fő csomópontok száma az ACS-fürtben.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationAdditionalProperties
A globális szolgáltatás konfigurációjának további tulajdonságai

```yaml
Type: Hashtable
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationETag
A frissítések beállítási ETag.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A operationalization-fürt tulajdonságai

```yaml
Type: PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A operationalization-fürt helye.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MasterCount
A fő csomópontok száma az ACS-fürtben.

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A operationalization-fürt neve.

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

### -OrchestratorType
Az ACS-fürt Orchestrator típusa.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A operationalization-fürt erőforráscsoport neve.

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

### -Secret
Az ACS-fürt Orchestrator szolgáltatásának fő titka.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
Az SSL-tanúsítványok a PEM formátumú, Base64-karakterláncként kódolt formában jelennek meg.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCName
Az SSL-tanúsítvány CName rekordja.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslKey
A PEM formátumú SSL-kulcsok a Base64-karakterláncként kódolt formában jelennek meg.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslStatus
SSL-állapot
A lehetséges értékek "engedélyezve" és "Letiltva".

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
A létrehozása helyett a tárolási fiók URI-ja.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## KIMENETEK

### Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

