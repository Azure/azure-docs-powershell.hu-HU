---
Module Name: AzureRM.HDInsight
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: fba8b9d96666a3a7d625e8f2af7274a6c086f94d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490588"
---
# AzureRM. HDInsight modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók. Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak. A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.

## AzureRM. HDInsight parancsmagok
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Felvesz egy biztonsági profileto a fürtkonfigurációs objektumba.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
HTTP-hozzáférést biztosít a fürthöz.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
RDP-elérést ad vissza a Windows-fürthöz.

### [Meghívó-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.

### [Új – AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.

### [Új – AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.

### [Új – AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Kaptár-objektumot hoz létre.

### [Új – AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Létrehoz egy MapReduce.

### [Új – AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Egy Pig-Job objektumot hoz létre.

### [Új – AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Létrehoz egy Sqoop.

### [Új – AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Adatfolyam-MapReduce hoz létre.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.

### [Visszavonás-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Letiltja a fürt HTTP-elérését.

### [Visszavonás-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Letiltja a Windows-fürtök RDP-elérését.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
A megadott szektorcsoportban lévő munkaállomások számát adja meg.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.

### [Stop-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Meghatározott futó feladat leállítása egy fürtben.

### [Submit-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.

### [Use-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.

### [Várjon-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
A megadott feladat befejezését vagy hibáját várja.

