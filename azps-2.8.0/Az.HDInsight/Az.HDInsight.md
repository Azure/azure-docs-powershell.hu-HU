---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 33e1e9ac0b62d378954280d8dd81361c0d075a1e
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665534"
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

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.

### [Grant-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
RDP-elérést ad vissza a Windows-fürthöz.

### [Meghívó-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.

### [Új – AzHDInsightCluster](New-AzHDInsightCluster.md)
Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.

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

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.

### [Visszavonás-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Letiltja a Windows-fürtök RDP-elérését.

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

