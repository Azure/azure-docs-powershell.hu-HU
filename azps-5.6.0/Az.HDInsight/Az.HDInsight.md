---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: ec924f7424d2b522e6bbd9ce1db51e8c920ec663
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938090"
---
# Az.HDInsight modul
## Leírás
A szakasz témakörei a Microsoft Azure HDInsight Azure PowerShell-parancsmagját, az Azure Resource Manager (ARM) keretrendszerben dokumentálják. Ezek a parancsmagok a HDInsight-fürtök és az őket futtató feladatok kezelésére használhatók. A parancsmagok a Microsoft.Azure.Commands.HDInsight névterében létezik.

## Az.HDInsight parancsmagok
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Fürtidentitás hozzáadása fürtkonfigurációs objektumhoz.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
A fürtben futó szolgáltatások verziójának hozzáadása fürtkonfigurációs objektumhoz.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
A Hadoop konfigurációs értékének és/vagy a Hive-tárak megosztott testreszabásának hozzáadása a fürtkonfigurációs objektumokhoz.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Egy fürtkonfigurációs objektumhoz hozzáad egy HIVE- vagy Oozie-metastoreként szolgáló SQL-adatbázist.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Parancsfájl-műveletet ad egy fürtkonfigurációs objektumhoz.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Biztonsági profil hozzáadása fürtkonfigurációs objektumhoz.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Hozzáad egy Azure-tárterületkulcsot egy fürtkonfigurációs objektumhoz.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
A HDInsight-fürtben való figyelés letiltása és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre fognak áramni.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
A HDInsight-fürtben való figyelés engedélyezése és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre lesznek küldve.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Beolvassa és felsorolja az aktuális előfizetéshez vagy adott erőforráscsoporthoz társított Összes Azure HDInsight-fürtöt, illetve lekér egy adott fürtöt.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
A HDInsight-fürt automatikus skálázási konfigurációját kapja meg.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
A HDInsight-fürt állomáslistái.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Beolvassa a feladatok listáját egy fürtből, és fordított időrendi sorrendben listázza őket, vagy lekér egy adott feladatot.

### [Get-AzHDInsightOutput](Get-AzHDInsightJobOutput.md)
Egy feladat naplókimenetét egy adott fürthöz társított tárfiókból kapja meg.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
A fürtön telepített telepítés figyelési állapotát kapja meg.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Lejátsa egy fürt megőrzött parancsprogram-műveletét, és időrendben felsorolja őket, vagy egy adott állandó parancsfájlművelet részleteit.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Beszerzheti a HDInsight szolgáltatás tulajdonságait, például az elérhető helyeket és a kapacitást.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Lekérte egy fürt parancsfájl-műveletelőzményét, és fordított időrendi sorrendben listázza azt, vagy egy korábban végrehajtott parancsprogram-művelet részleteit.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Hive-lekérdezést küld egy HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Azure HDInsight-fürtöt hoz létre a megadott erőforráscsoportban az aktuális előfizetéshez.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Egy nem állandó objektumot hoz létre, amely leírja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Automatikus ütemezési feltételt hoz létre.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Olyan nem állandó fürtkonfigurációs objektumot hoz létre, amely leírja az Azure HDInsight-fürtkonfigurációt.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Létrehoz egy Hive-feladatobjektumot.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
MapReduce-feladatobjektumot hoz létre.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Ezzel a beállításokkal egy feladatobjektumot hoz létre.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Létrehoz egy Sqoop feladatobjektumot.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Létrehozza a Streaming MapReduce feladatobjektumot.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
A megadott HDInsight-fürt eltávolítása az aktuális előfizetésből.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
A HDInsight-fürt automatikus skálázási konfigurációjának eltávolítása.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Egy megőrzött parancsfájl-műveletet eltávolít egy HDInsight-fürtből.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Újraindítja a HDInsight-fürt adott állomását.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Beállítja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
A megadott HDInsight-fürt lemeztitkosítási kulcsának elforgatása.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Beállítja egy adott fürt dolgozói csomópontjainak számát.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Egy fürtkonfigurációs objektum alapértelmezett tárfiók-beállítását állítja be.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Beállítja egy Azure HDInsight-fürt átjáró HTTP-hitelesítő adatait.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Egy korábban végrehajtott parancsfájl-műveletet állandó parancsfájl-műveletként állít be.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Egy megadott Azure HDInsight-feladatot kezd egy adott fürtön.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Leállít egy megadott futó feladatot egy fürtön.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
A parancsmaggal együtt használni kívánt Invoke-RmAzureHDInsightHiveJob kijelölése.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Megvárja egy adott feladat elvégzését vagy sikertelenségét.

