---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 035b21684c3d8fc64cee7ee78b7b4cb2adf21f01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836097"
---
# Add-AzHDInsightClusterIdentity

## Áttekintés
A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.

## SZINTAXISA

### CertificateFilePath (alapértelmezett)
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CertificateFileContents
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzHDInsightClusterIdentity** parancsmag a New-AzHDInsightClusterConfig parancsmag által létrehozott Azure HDInsight Configuration objektumhoz ad egy fürtöt.

## Példák

### 1. példa: a fürtkonfigurációs adatok felvétele a fürtkonfigurációs objektumba
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

Ez a parancs a cluster Identity-adatokat hozzáadja a-Hadoop-001 nevű fürthöz, így a klaszter hozzáférhet az Azure Data Lake Store szolgáltatáshoz.

## PARAMÉTEREK

### -AadTenantId
Az Azure AD bérlői AZONOSÍTÓját adja meg, amelyet az Azure Data Lake Store elérésekor fog használni.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFileContents
Az Azure Data Lake Store-hoz való hozzáféréshez használt tanúsítvány fájljának tartalmát adja meg.

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFilePath
Annak a tanúsítványnak a fájl elérési útvonalát adja meg, amelyet a rendszer a szolgáltatóként való hitelesítéshez fog használni.
A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Annak a tanúsítványnak a jelszava, amelyet a rendszer a szolgáltatóként való hitelesítéshez használni fog.
A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.
Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag hozza létre.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -ObjectId
Megadja a fürtöt képviselő Azure ad Object azonosító (GUID) azonosítót.
A fürt ezt fogja használni az Azure Data Lake Store eléréséhez.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig

### System. GUID

## KIMENETEK

### Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzHDInsightClusterConfig](./New-AzHDInsightClusterConfig.md)


