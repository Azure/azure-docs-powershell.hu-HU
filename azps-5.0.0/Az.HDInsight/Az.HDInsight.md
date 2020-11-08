---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185383"
---
# Az. HDInsight modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók. Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak. A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.

## Az. HDInsight parancsmagok
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Biztonsági profilt ad hozzá a fürtkonfiguráció-objektumhoz.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Letiltja a figyelést egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott figyelési munkaterületre áramlanak.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Lehetővé teszi a HDInsight-fürtök figyelését, és a megfelelő naplók az engedélyezés során megadott figyelési munkaterületre kerülnek.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Beilleszti a HDInsight-fürt automatikus méretarányos konfigurációját.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Felsorolja a HDInsight-fürt állomásait.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
A telepítés figyelésének állapotát kapja meg a fürtben.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.

### [Meghívó-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.

### [Új – AzHDInsightCluster](New-AzHDInsightCluster.md)
Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.

### [Új – AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtök automatikus méretarányos konfigurációját.

### [Új – AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Ütemezési alapú autoscale-feltételt hoz létre.

### [Új – AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.

### [Új – AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Kaptár-objektumot hoz létre.

### [Új – AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Létrehoz egy MapReduce.

### [Új – AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Egy Pig-Job objektumot hoz létre.

### [Új – AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Létrehoz egy Sqoop.

### [Új – AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Adatfolyam-MapReduce hoz létre.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Eltávolítja a HDInsight-fürt automatikus méretezési konfigurációját.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.

### [Újraindítás – AzHDInsightHost](Restart-AzHDInsightHost.md)
A HDInsight-fürt adott állomásainak újraindítása.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Az Azure HDInsight-fürtök automatikus méretarányos konfigurációjának beállítása.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Elforgatja a megadott HDInsight-fürt lemez titkosítási kulcsát.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
A megadott szektorcsoportban lévő munkaállomások számát adja meg.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Az Azure HDInsight-fürtök átjárójának HTTP-hitelesítő adatait állítja be.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Meghatározott futó feladat leállítása egy fürtben.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.

### [Várjon-AzHDInsightJob](Wait-AzHDInsightJob.md)
A megadott feladat befejezését vagy hibáját várja.

