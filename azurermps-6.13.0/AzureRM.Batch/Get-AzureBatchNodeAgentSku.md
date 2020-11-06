---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 86451c1ac7ba52c9b013b3724d9c706caaa961ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492009"
---
# Get-AzureBatchNodeAgentSku

## Áttekintés
Köteg-csomópont ügynöki SKU-t kap egy köteg fiókban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureBatchNodeAgentSku** parancsmag az Azure-alapú köteg fiókokban elérhető, csomópont-ügynököt tartalmazó SKU-t kapja.
Adja meg a fiókot a *BatchContext* paraméter használatával.
Szűkítheti a keresést olyan SKU-ra, amely megfelel egy Open Data Protocol (OData) szűrőnek.

## Példák

### 1. példa: az összes elérhető csomópont ügynöki SKU beszerzése
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

Az első parancs a **Get-AzureRmBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.
A parancs a következő parancsban a $Context változó környezetét tárolja.
A második parancs beolvassa az összes elérhető Node Agent SKU-t, amelyet a köteg támogat.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Szűrő
A OData-szűrési záradékot adja meg a Node Agent SKU-hoz.
Ha nem ad meg szűrőt, a parancsmag minden olyan csomópont-ügynököt visszaad, amelyet a köteg támogat.

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

### -MaxCount
Azt adja meg, hogy legfeljebb hány csomópontos SKU-t szeretne visszaadni.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Paraméterek: BatchContext (ByValue)

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSNodeAgentSku

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)


