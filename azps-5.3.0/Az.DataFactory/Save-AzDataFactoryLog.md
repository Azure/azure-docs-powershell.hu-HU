---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480393"
---
# <span data-ttu-id="0f00f-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="0f00f-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="0f00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f00f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f00f-103">Naplófájlokat tölt le az Azure HDInsight-feldolgozásból.</span><span class="sxs-lookup"><span data-stu-id="0f00f-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="0f00f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f00f-104">SYNTAX</span></span>

### <span data-ttu-id="0f00f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f00f-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f00f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0f00f-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f00f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f00f-107">DESCRIPTION</span></span>
<span data-ttu-id="0f00f-108">A **Save-AzDataFactoryLog** parancsmag letölti a vírus- vagy hive-projektek Azure HDInsight-feldolgozásával vagy egyéni tevékenységekkel kapcsolatos naplófájlokat a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="0f00f-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="0f00f-109">Először a Get-AzDataFactoryRun-parancsmag futtatásával lekéri egy tevékenység azonosítóját egy adatszelethez, majd ezzel az azonosítóval beolvassa a naplófájlokat a HDInsight-fürttel társított bináris nagy objektum (BLOB) tárolóból.</span><span class="sxs-lookup"><span data-stu-id="0f00f-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="0f00f-110">Ha nem adja meg *a DownloadLogs* paramétert, a parancsmag csak a naplófájlok helyét adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0f00f-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="0f00f-111">Ha a *DownloadLogs paramétert* kimeneti könyvtár *(kimeneti* paraméter) megadása nélkül adja meg, a naplófájlok az alapértelmezett Dokumentumok mappába kerülnek.</span><span class="sxs-lookup"><span data-stu-id="0f00f-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="0f00f-112">Ha a *DownloadLogs mappát* egy kimeneti mappával *(Kimenet)* együtt adja meg, a naplófájlok a megadott mappába kerülnek.</span><span class="sxs-lookup"><span data-stu-id="0f00f-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="0f00f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f00f-113">EXAMPLES</span></span>

### <span data-ttu-id="0f00f-114">1. példa: Naplófájlok mentése egy adott mappába</span><span class="sxs-lookup"><span data-stu-id="0f00f-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="0f00f-115">Ez a parancs a 841b77c9-d56c-48d1-99a3-8c16c3e77d39 azonosítóval menti a tevékenységhez tartozó naplófájlokat, ahol a tevékenység az ADF nevű erőforráscsoport LogProcessingFactory nevű adat factoryjának egyik folyamatába tartozik.</span><span class="sxs-lookup"><span data-stu-id="0f00f-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="0f00f-116">A naplófájlokat a rendszer a C:\Test mappába menti.</span><span class="sxs-lookup"><span data-stu-id="0f00f-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="0f00f-117">2. példa: Naplófájlok mentése az alapértelmezett Dokumentumok mappába</span><span class="sxs-lookup"><span data-stu-id="0f00f-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="0f00f-118">Ez a parancs a naplófájlokat a Dokumentumok mappába (alapértelmezés szerint) menti.</span><span class="sxs-lookup"><span data-stu-id="0f00f-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="0f00f-119">3. példa: A naplófájlok helyének lekérte</span><span class="sxs-lookup"><span data-stu-id="0f00f-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="0f00f-120">Ez a parancs a naplófájlok helyét adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0f00f-120">This command returns the location of log files.</span></span>
<span data-ttu-id="0f00f-121">Ne feledje, *hogy a DownloadLogs* nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0f00f-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="0f00f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f00f-122">PARAMETERS</span></span>

### <span data-ttu-id="0f00f-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0f00f-123">-DataFactory</span></span>
<span data-ttu-id="0f00f-124">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="0f00f-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="0f00f-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f00f-125">-DataFactoryName</span></span>
<span data-ttu-id="0f00f-126">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f00f-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0f00f-127">Ez a parancsmag letölti a paraméter által megadott adatüzem naplófájlját.</span><span class="sxs-lookup"><span data-stu-id="0f00f-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f00f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f00f-128">-DefaultProfile</span></span>
<span data-ttu-id="0f00f-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f00f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f00f-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="0f00f-130">-DownloadLogs</span></span>
<span data-ttu-id="0f00f-131">Azt jelzi, hogy ez a parancsmag letölti a naplófájlokat a helyi számítógépre.</span><span class="sxs-lookup"><span data-stu-id="0f00f-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="0f00f-132">Ha *nincs* megadva kimeneti mappa, a program a fájlokat egy almappa Dokumentumok mappájába menti.</span><span class="sxs-lookup"><span data-stu-id="0f00f-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="0f00f-133">-Id</span><span class="sxs-lookup"><span data-stu-id="0f00f-133">-Id</span></span>
<span data-ttu-id="0f00f-134">Az adatszelethez futtatott tevékenység azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f00f-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="0f00f-135">A Get-AzDataFactoryRun parancsmag használatával lekérte az azonosítót.</span><span class="sxs-lookup"><span data-stu-id="0f00f-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="0f00f-136">-Kimenet</span><span class="sxs-lookup"><span data-stu-id="0f00f-136">-Output</span></span>
<span data-ttu-id="0f00f-137">Azt a kimeneti mappát adja meg, amelybe a letöltött naplófájlok mentve vannak.</span><span class="sxs-lookup"><span data-stu-id="0f00f-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="0f00f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f00f-138">-ResourceGroupName</span></span>
<span data-ttu-id="0f00f-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f00f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0f00f-140">Ez a parancsmag létrehoz egy adatüzemet, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0f00f-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f00f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f00f-141">CommonParameters</span></span>
<span data-ttu-id="0f00f-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f00f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f00f-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f00f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f00f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f00f-144">INPUTS</span></span>

### <span data-ttu-id="0f00f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0f00f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0f00f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0f00f-146">System.String</span></span>

## <span data-ttu-id="0f00f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f00f-147">OUTPUTS</span></span>

### <span data-ttu-id="0f00f-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="0f00f-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="0f00f-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f00f-149">NOTES</span></span>
* <span data-ttu-id="0f00f-150">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="0f00f-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0f00f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f00f-151">RELATED LINKS</span></span>

[<span data-ttu-id="0f00f-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="0f00f-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="0f00f-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0f00f-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0f00f-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0f00f-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="0f00f-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0f00f-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="0f00f-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0f00f-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="0f00f-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0f00f-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


