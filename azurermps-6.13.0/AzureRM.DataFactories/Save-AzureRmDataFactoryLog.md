---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 41b147307d253271e24667bd61d827c245f4500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672977"
---
# <span data-ttu-id="19652-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="19652-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="19652-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19652-102">SYNOPSIS</span></span>
<span data-ttu-id="19652-103">Az Azure HDInsight-feldolgozásból letölthető naplófájlok.</span><span class="sxs-lookup"><span data-stu-id="19652-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19652-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19652-104">SYNTAX</span></span>

### <span data-ttu-id="19652-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19652-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19652-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="19652-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19652-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19652-107">DESCRIPTION</span></span>
<span data-ttu-id="19652-108">A **Save-AzureRmDataFactoryLog** parancsmag letölti az Azure HDInsight-szal kapcsolatos, a sertés-vagy a kaptár-projektek vagy az egyéni tevékenységek helyi merevlemezre való kezelését okozó naplófájlokat.</span><span class="sxs-lookup"><span data-stu-id="19652-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="19652-109">Először futtatja az Get-AzureRmDataFactoryRun parancsmagot egy adatszelethez tartozó tevékenység AZONOSÍTÓjának beolvasásához, majd ezt az azonosítót használva beolvashatja a naplófájlokat a HDInsight-fürthöz társított bináris nagy objektum (BLOB) tárolóból.</span><span class="sxs-lookup"><span data-stu-id="19652-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="19652-110">Ha nem adja meg a *DownloadLogs* paramétert, a parancsmag csak a naplófájlok helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19652-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="19652-111">Ha a *DownloadLogs* megadása nélkül adja meg a kimeneti könyvtárat ( *kimeneti* paraméter), a rendszer letölti a naplófájlokat az alapértelmezett dokumentumok mappába.</span><span class="sxs-lookup"><span data-stu-id="19652-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="19652-112">Ha a *DownloadLogs* a kimeneti mappával ( *output* ) együtt adja meg, a rendszer letölti a naplófájlokat a megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="19652-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="19652-113">Példák</span><span class="sxs-lookup"><span data-stu-id="19652-113">EXAMPLES</span></span>

### <span data-ttu-id="19652-114">1. példa: naplófájlok mentése egy adott mappába</span><span class="sxs-lookup"><span data-stu-id="19652-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="19652-115">Ez a parancs menti a tevékenység naplófájlját azzal az AZONOSÍTÓval, ahol a tevékenység az ADF nevű erőforráscsoport LogProcessingFactory nevű 841b77c9-d56c-48d1-99a3-8c16c3e77d39 tartozik.</span><span class="sxs-lookup"><span data-stu-id="19652-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="19652-116">A naplófájlok a C:\Test mappába kerülnek.</span><span class="sxs-lookup"><span data-stu-id="19652-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="19652-117">2. példa: naplófájlok mentése az alapértelmezett dokumentumok mappába</span><span class="sxs-lookup"><span data-stu-id="19652-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="19652-118">Ez a parancs naplófájlokat ment a dokumentumok mappába (alapértelmezett).</span><span class="sxs-lookup"><span data-stu-id="19652-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="19652-119">3. példa: naplófájlok helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="19652-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="19652-120">Ez a parancs a naplófájlok helyét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="19652-120">This command returns the location of log files.</span></span>
<span data-ttu-id="19652-121">Figyelje meg, hogy a *DownloadLogs* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="19652-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="19652-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19652-122">PARAMETERS</span></span>

### <span data-ttu-id="19652-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="19652-123">-DataFactory</span></span>
<span data-ttu-id="19652-124">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="19652-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19652-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="19652-125">-DataFactoryName</span></span>
<span data-ttu-id="19652-126">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19652-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="19652-127">Ez a parancsmag letölti az adatfeldolgozó naplófájlját, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="19652-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19652-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19652-128">-DefaultProfile</span></span>
<span data-ttu-id="19652-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19652-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19652-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="19652-130">-DownloadLogs</span></span>
<span data-ttu-id="19652-131">Jelzi, hogy a parancsmag a naplófájlokat letölti a helyi számítógépre.</span><span class="sxs-lookup"><span data-stu-id="19652-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="19652-132">Ha a *ouptut* mappa nincs megadva, a fájlok a dokumentumok mappába kerülnek a mappa almappájában.</span><span class="sxs-lookup"><span data-stu-id="19652-132">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="19652-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="19652-133">-Id</span></span>
<span data-ttu-id="19652-134">Az adatszelethez futtatott tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19652-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="19652-135">A Get-AzureRmDataFactoryRun parancsmag használatával kaphat azonosítót.</span><span class="sxs-lookup"><span data-stu-id="19652-135">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19652-136">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="19652-136">-Output</span></span>
<span data-ttu-id="19652-137">Azt a kimeneti mappát adja meg, amelyben a letöltött naplófájlok vannak mentve.</span><span class="sxs-lookup"><span data-stu-id="19652-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19652-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19652-138">-ResourceGroupName</span></span>
<span data-ttu-id="19652-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19652-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="19652-140">Ez a parancsmag olyan adattípust hoz létre, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="19652-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19652-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19652-141">CommonParameters</span></span>
<span data-ttu-id="19652-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19652-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19652-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19652-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19652-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19652-144">INPUTS</span></span>

### <span data-ttu-id="19652-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="19652-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="19652-146">System. String</span><span class="sxs-lookup"><span data-stu-id="19652-146">System.String</span></span>

## <span data-ttu-id="19652-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19652-147">OUTPUTS</span></span>

### <span data-ttu-id="19652-148">Microsoft. Azure. Command. DataFactories. models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="19652-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="19652-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19652-149">NOTES</span></span>
* <span data-ttu-id="19652-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="19652-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="19652-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19652-151">RELATED LINKS</span></span>

[<span data-ttu-id="19652-152">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="19652-152">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="19652-153">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="19652-153">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="19652-154">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="19652-154">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="19652-155">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="19652-155">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="19652-156">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="19652-156">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="19652-157">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="19652-157">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


